---
layout: post
title:      "Getting Comfortable With AJAX"
date:       2018-07-23 19:52:02 +0000
permalink:  getting_comfortable_with_ajax
---

This one was a little different from earlier projects. I felt like I was programming more logically and finding my flow. AJAX syntax itself wasn't nearly as hard as trying to get it to cooperate with the Rails framework. At times, I found myself resenting the implicit nature of Rails when working with an non-Ruby outside language. Sometimes, explicit instructions just work best. The biggest challenge of this project was trying to get AJAX to render properly within a view that could be reused in different routes. For example, I have a Benefits model. This model's index was accessed both on the base level of the application, as well as nested within the Users route. Each view was to be rendering Benefits, but one was going to be filtered by a User's Selections. In order to achieve this, I ended up setting a variable in the Benefits controller, passing it to the view, and in turn, setting it via Javascript to send to the asset pipeline as needed, once the view was rendered. I used Handlebars to inject the returned JSON data directly to the DOM by templating my injection HTML in a script tag below my content. I found that utilizing partials made my code easier to customize, as well as keeping it better organized. Overcoming the challenges in this project led me to have a greater confidence in my coding ability and to help find strength to break through challenging roadblocks. 
