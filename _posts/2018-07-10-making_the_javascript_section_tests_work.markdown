---
layout: post
title:      "Making the Javascript section tests work."
date:       2018-07-10 18:15:08 +0000
permalink:  making_the_javascript_section_tests_work
---


I noticed when I was in the Javascript labs that I was having an error and my tests weren't running properly.

`index "before all" hook: Error: Cannot find module 'jsdom/lib/old-api'`


1. Open package.json


2. Scroll down to "dependencies" and change line:

 ` "mocha-jsdom": "^1.1.0",` to `"mocha-jsdom": "2.0.0",`, save file.


3. In terminal, type npm install.


That's it! 
