---
layout: post
title:      "How to set up with Devise to accept a username instead of email"
date:       2018-03-05 21:19:19 -0500
permalink:  rails_with_jquery_project
---

To my surprise, when I pulled up my existing Rails app to add a JQuery front-end, I ended up spending the first few days fixing features that had broken: mainly, Omniauth (which I can already tell will be the bane of my existence). I had set up my Omniauth to work with Twitter. Back when I had created my Rails app, everything was running swimmingly -- I had users choosing to sign in with either their email address/password or their Twitter account. When I tested this feature again last week, I was getting an error. After some research, I discovered that Twitter only sends over the user's **username**, not their email address - hence why the app was breaking. 

It took a LOT of work and a lot of troubleshooting, but I eventually learned how to tailor Devise to accept just usernames and passwords -- no email necessary. In order to hopefully prevent anyone else from experiencing this headache, here are the steps (in no particular order):

If you already set up Devise with a User model like I had, the process mainly involves a lot of modifications to the existing files.

***User model modifications***

A) In your User model, under devise:
     1) **delete** :validatable (**this is VERY important and will cause the app to break if not done!!)**
     2) add :authentication_keys => [:username]

B) Twitter sends over the user's username under the key 'nickname'. Therefore, you have to edit the User model's **self.from_omniauth** method accordingly:
```
        def self.from_omniauth(auth)
           where(provider: auth.provider, uid: auth.uid).first_or_create do |user|
           user.**username** = auth.info.**nickname**
           user.password = Devise.friendly_token[0,20]
           end
         end
```

C) Since you've deleted :validatable from the devise features in the User model, you'll need to create your own validations. This is done by adding **validates :username, uniqueness: true** to the User model.

**View folder modifications**

This was the trickiest for me to figure out, as generating Devise for my users didn't automatically create a views folder for devise. Therefore, I had to manually generate that folder by typing **rails generate devise:views User** into my terminal. That revealed my devise views folder.

A) In the Views:Devise:Sessions folder, edit the new.html.erb file by swapping the email address form fields with username.

B) In the Views:Devise:Registrations folder, do the exact same with both the new.html.erb and edit.html.erb files.

**Config modifications**

Next, you'll need to go to the Config:Initializers:devise.rb file.

A) Replace ANY mention of :email with :username. Except for **config.email_regexp = /\A[^@\s]+@[^@\s]+\z/.** That can stay the same.

**DB modifications**

Last but not least, you need to change the users database.

A) Drop any references to email -- this includes both the string and the index. 

B) Create the following migration:

```
class AddUsernameToUsers < ActiveRecord::Migration[4.2]
  def change
    add_column :users, :username, :string, null: false, default: ""
  end

  add_index :users, :username, unique: true
end
```

Remember to rake db:migrate!

And there you have it! Twitter and Omniauth should now be talking to each other swimmingly. 
     

