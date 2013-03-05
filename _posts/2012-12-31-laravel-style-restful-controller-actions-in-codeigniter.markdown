---
comments: true
date: 2012-12-31 19:54:01
layout: post
slug: laravel-style-restful-controller-actions-in-codeigniter
title: Laravel Style RESTful Controller Actions in CodeIgniter
wordpress_id: 147
categories:
- Web Development
tags:
- best practice
- codeigniter
- laravel
- php
- tips
---

[Laravel](http://laravel.com) has really hooked me over the last year and I even have decided to never look back to [CodeIgniter (CI)](http://codeigniter.com) anymore since then. But unfortunately, I recently got a web development job that still using ancient PHP version Laravel doesn't (and never been) support :(

Definitely, using Laravel (and peeking at its core source code) has taught me many advanced PHP things and how web development should better be. Laravel's clean and expressive syntax is a real breeze and made me realized (and a lil bit disgusted) how ugly CodeIgniter style was when I have to work with it again after a long time.

This time I will show you [a trick I found](http://www.toddandrae.com/?p=95) and modified a little to conform Laravel's style I've been used to enjoy. Let's get started ;)

<!-- more -->

Consider the following CodeIgniter styled controller actions:

    
    class Article extends CI_Controller {
    
    	public function add()
    	{
    		if($this->input->post('submit'))
    		{
    			// Process the form inputs
    			// then redirect to success page
    		}
    		else
    		{
    			// Show the form
    		}
    	}
    
    }


Laravel's controller has a feature that called RESTful controllers/actions that separates route mapping to different methods based on the HTTP request (post, get, put, delete, etc) made. Take a look at this one:

    
    class Article extends Controller {
    
    	public $resful = true;
    
    	public function get_add()
    	{
    		// Show the form
    	}
    
    	public function post_add()
    	{
    		// Process the form inputs
    		// then redirect to success page
    	}
    
    }


Elegant, isn't it? That way we can keep the URL for forms and processing the same yet preventing multiple form submission while keeping the code clean.  The route 'article/add' (assuming we're using standard route-action mapping) mapping will splitted to to different methods based on the HTTP request made by user. It will route to get_add() if the request is GET, and get_post() if it's a POST one. Pretty clear, huh?


#### Here's the trick


We can get the same effect in CodeIgniter by using custom router class [as pointed by Todd in his article](http://www.toddandrae.com/?p=95). I just modified the code a little to mimic Laravel more. So we started by a custom class, create a file in 'application/core' named 'MY_Router.php'

    
    class MY_Router extends CI_Router {
    	function fetch_method()
    	{
    		$request = strtolower($_SERVER['REQUEST_METHOD']);
    
    		if ($this->method == $this->fetch_class()) 
    		{
    			$method = $request.'_index';
    		} 
    		else 
    		{
    			$method = $request.'_'.$this->method;
    		}
    
    		return $method;
    	}
    }


That's all! Now you get the same functionality as Laravel's RESTful Controller in CodeIgniter.



---

Credit: [Request Specific CodeIgniter Methods](http://www.toddandrae.com/?p=95) by Todd Andrae
