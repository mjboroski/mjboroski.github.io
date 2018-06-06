---
layout: post
title:      "Rolling back the activerecord gem to version 4.2"
date:       2018-06-06 20:26:33 +0000
permalink:  rolling_back_the_activerecord_gem_to_version_4_2
---


As I tried to run tests on the "User Authentication in Sinatra" codealong in my IDE, I kept running into an error. 

```
NoMethodError: undefined method `needs_migration?' for ActiveRecord::Migrator:Class
```

Upon a quick google search for the error with no relevant results, it seemed I was on my own. I took the results and tried to piece together an answer from nothing. It seemed many of these results were problems with version control. On a hunch, I changed a line in my Gemfile.  I rolled back the activerecord gem to version 4.2.

```
gem 'activerecord', '4.2'
```

I tried running my tests again. No luck, but a new message: 

```
You have requested:
  activerecord = 4.2
The bundle currently has activerecord locked at 5.2.0.
Try running `bundle update activerecord`
```

I updated the bundle and at the end, I saw this line in yellow: 

`Bundler attempted to update activerecord but its version regressed from 5.2.0 to 4.2.0`

I had a good feeling that things were about to work, so I ran my tests once more and this time they executed. 

In summary, I learned that the version changes from activerecord 4.2 to 5.2 broke the program. It seems a function called "nneds_migration?" was eliminated  in the updates, causing the test suite to throw an error in execution.
