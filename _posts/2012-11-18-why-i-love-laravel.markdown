---
comments: true
date: 2012-11-18 23:19:03
layout: post
slug: why-i-love-laravel
title: Why I Love Laravel
wordpress_id: 80
categories:
- Web Development
tags:
- laravel
- php
---

> Laravel is a clean and classy framework for PHP web development. Freeing you from spaghetti code, Laravel helps you create wonderful applications using simple, expressive syntax. Development should be a creative experience that you enjoy, not something that is painful. Enjoy the fresh air.


Recently I have been moved from CodeIgniter (CI) to Laravel even for production uses. Well, I cannot fully move away from CI since it's unavoidable the most used PHP framework nowadays. My curiousity started when my friend barely mentioned Laravel in a chat. I gave it a try by looking at the online docs and it turned out to be more and more interesting. Here I will highlight some of the features of Laravel that I love and you should too.

<!-- more -->


# Elegant Code


Using CI for several production times then trying Laravel made me realize how ugly my code was. Instead of singleton pattern that CI uses, Laravel which was born in PHP 5.3+ era make extensive uses of static methods, anonymous functions, method chains, and namespaces.

Some example:

    
    // CI version on creating view
    return $this->load->view('user/single', array('data' => $data));
    
    // Laravel's version on creating view
    return View::make('user.single')->with('user', $user);
    
    // Analogous to CI's anchor function
    HTML::link('post/'.$post->id, $post->title);
    
    // Get all the posts from DB and cache it for 10 minutes
    // will skip DB call if the cache still exists 
    $posts = Cache::remember('posts', function(){
        return Post::all();
    }, 10);




# Class Autoloading




> Class Auto Loading keeps you from having to maintain an autoloader configuration and from loading unnecessary components when they won't be used. Want to use a library or model? Don't bother loading it, just use it. Laravel will handle the rest.


Pretty clear, we don't need manually define every libraries, models, or helper to be loaded. Laravel handles all of these messy task. All the classes are lazy-loaded, means that they won't be loaded until used.


# Database Migration




> Migrations are version control for your database schemas and they are directly integrated into Laravel. You can both generate and run migrations using the "Artisan" command-line utility. Once another member makes schema changes you can update your local copy from the repository and run migrations. Now you're up to date, too!


Now I cannot live without this. DB migration solve most of the problems with database design revisions when working with team. Instead of working directly with database (i.e. via PhpMyAdmin) and sharing the raw SQL create+insert file with teammates, we can just design the tables creation and destruction script directly in the application code. That means the database structures can be versioned with SVN, Git, or other VCSes. Additionally, because the table create scripts are written in Laravel's class  that also mean your application is almost DBMS-agnostic. Change a little connection configuration and it's work on other DBMS that supported by Laravel (or external bundles).

Sample:

    
    class Tables {
    
    	/**
    	 * Make changes to the database.
    	 *
    	 * @return void
    	 */
    	public function up()
    	{
    		Schema::create('users', function($table){
    			$table->increments('id');
    			$table->string('username', 20);
    			$table->string('email', 100);
    			$table->string('password', 100);
    			$table->string('fullname', 100);
    			$table->timestamps();
    		});
    	}
    
    	/**
    	 * Revert the changes to the database.
    	 *
    	 * @return void
    	 */
    	public function down()
    	{
    		Schema::drop('users');
    	}
    
    }




I will add more about Eloquent, Laravel's charming ORM later :)
