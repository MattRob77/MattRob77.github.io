---
layout: post
title:      "It's Sinatra Time!! "
date:       2019-10-30 20:14:45 +0000
permalink:  its_sinatra_time
---


![](http://giphygifs.s3.amazonaws.com/media/k0SPYuMizvN5e/giphy.gif)

This Sinatra web application should include:
* utilize CRUD and MVC structure 
* Validate uniqueness of user login 
* let users edit and delete  their own resources
* users ability to sign up, sign in, and sign out
* content management system (CMS)
* Shows single responsibility principle  

When I was reading the requirements for this project I knew I wanted to do something that could be valuable to me and provide value to someone I care for, my wife. My wife is a very structured person, so I knew I wanted to create a task planner that would track a users task. 

![](https://media.giphy.com/media/3ornk5GCUXm1TklS0M/giphy.gif) 

Ok, time to focus! This sinatra application called " Task Planner" would be a place for users to join so they can keep track of daily tasks and what-to-dos. Now that I know what the bases of my application would be it's time to build it. 

****Getting Started **** 

The steps I took in building this web application: 

1. Built file structure using Corneal Gem(handy gem that creates basic structure) 
2. Uploaded all my gems I needed to run my application 
3. Built out my ApplicationController
4. Started my migrations for users and the tasks  
5. Built out my models - the User and Task. (belongs_to:user) (has_many :tasks) 
6. Built out the views which I spent most of my time figuring out HTML tags and ERB tags (<%=    %>) 

![](https://media.giphy.com/media/aYPQnBpHb9Neg/giphy.gif) 

**Not Done Yet!**

7. Updated my controllers adding session secret(told there was a way to change it into environment file) 
8. Built out the highly important "Config .ru" this file helps being able to run the app like Sinatra 
9.  Added Rack:MethodOverride in order to use Patch, Put, and Delete requests. 

```
require './config/environment'

if ActiveRecord::Migrator.needs_migration?
  raise 'Migrations are pending. Run `rake db:migrate` to resolve the issue.'
end

use Rack::MethodOverride
run ApplicationController
use TasksController
use SessionsController
use UsersController 
```

10. Added Rake_File to be able to run my ActiveRecord migrations 

**Getting Closer**  

11. Added Authentication to keep my app safe from outside non users and to help protect current users(Used redirects) 
12. Added some validations to make sure user was more protected 

![](https://media.giphy.com/media/l0IycQmt79g9XzOWQ/giphy.gif) 

Looking forward to learning more about Rails and other programs so I can continue to build this out to make it better. There are some things I would add like being able to check tasks off instead of having to delete the task. Also, want to continue to learn more about front end to be able to add more styling CSS to my applications. Overall this was a good experience to learn the structure of an application and how to organize my workflow. Next it's Rails!!! 

![](https://media.giphy.com/media/14sIASsr4noLug/giphy.gif) 










