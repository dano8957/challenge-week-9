# Name

Daniel Nolan

# How many points have you earned?

76/100

(Make your own calculation and replace the number 0 with the points you think you've earned.)

# How many hours have you spent on this?

~7

# When did you first start working on this week's learning challenges?

Saturday night

# What is the most difficult part about this week's challenge?

So far it was getting my .js file from Week 6 to list off all events from the start of our CSCI-4830 class. I looked online and utilized resources to finally figure it out though. I had some minor bracket issues with the MongoDB commands but easily found and fixed those issues.

# Show and tell (8 points)

## Link (2 points)

[Big data and machine learning's sleeping giant](http://www.upi.com/Technology/2014/10/22/0xdata-Big-data-and-machine-learnings-sleeping-giant/8011414022038/)

## Discuss how you may apply the machine learning technique mentioned in this article to another interesting problem (6 points).

As stated in the video provided within the link, an example of H20 use was if your business was trying to find the best product placement for your website to get the best customer ratings and performance on this created site. The use of H20 will simplify large amount of H20 through machine learning processes that were built from the bottom up. You want to model the interactions of your customers into the future interactions that they will have relative to your products. H20 will allow hundreds of models in nanoseconds to be sampled through the algorithms implemented in this program. It will quickly allow you to test datasets on the possible predictions of what your customers will want next in a product.

# D3 IV

## Checkpoints (3 points x 4 = 12 points)

# 1. (3 points)

![image](image.png?raw=true)

[checkpoint](checkpoint.html)

# 2. (3 points)

![image](image.png?raw=true)

[checkpoint](checkpoint.html)

# 3. (3 points)

![image](image.png?raw=true)

[checkpoint](checkpoint.html)

# 4. (3 points)

![image](image.png?raw=true)

[checkpoint](checkpoint.html)

## Challenges (4 points x 3 = 12 points)

# 1. (4 points)

![image](image.png?raw=true)

# 2. (4 points)

![image](image.png?raw=true)

# 3. (4 points)

![image](image.png?raw=true)

[challenge3](challenge3.html)



# MongoDB II

## Checkpoints (6 points x 2 = 12 points)

### 1 (6 points)

[mongodb js code collecting github events about our course](mongodb-github.js)

### 2 (6 points)

![terminal output of mongodb query](http://i.imgur.com/CwSS1As.png)

## Challenge 1 (4 points x 10 = 40 points)

### 1 (4 points)

> db.course_events.findOne({"actor.login" : "doubleshow"}); 

![screenshot](http://i.imgur.com/myWyI6m.png)

### 2 (4 points)

> db.course_events.findOne({"actor.login" : "doubleshow"},{"actor" : "1"});

![screenshot](http://i.imgur.com/VuiVLcV.png)

### 3 (4 points)

> db.course_events.findOne({"actor.login" : {$in : ["doubleshow","chrisbopp"]}},{"actor.login" : "1", "created_at" : 1});

![screenshot](http://i.imgur.com/Ip4Ny8J.png)

### 4 (4 points)

> db.course_events.findOne({'type' : 'PushEvent'})

![screenshot](http://i.imgur.com/MEGcUeQ.png)

### 5 (4 points)

> db.course_events.findOne({'type' : {$in : ['PushEvent']}},{"payload.commits.author.name" : "1"});

![screenshot](http://i.imgur.com/Wc5xEDx.png)

### 6 (4 points)

> db.course_events.findOne({'type' : {$in : ['IssuesEvent']}});

![screenshot](http://i.imgur.com/A2Lj9h0.png)

### 7 (4 points)

> db.course_events.find({'type' : {$in : ['IssuesEvent']}},{'payload.issue.user.login'  : 1});

![screenshot](http://i.imgur.com/piO7RXW.png)

### 8 (4 points)

> db.course_events.find({'type' : {$in : ['IssuesEvent']},"payload.issue.state"  : "closed"},{"payload.issue.user.login":1,"payload.issue.state":1})

![screenshot](http://i.imgur.com/DM7FMrL.png)

### 9 (4 points)

> db.course_events.find({'type' : {$in : ['IssuesEvent']},"payload.issue.state"  : "open"},{"payload.issue.user.login":1,"payload.issue.state":1})

![screenshot](http://i.imgur.com/YaqohDj.png)

### 10 (4 points)

> db.course_events.find({'type' : {$in : ['IssuesEvent']},"payload.issue.comments" : {$gt : 0}},{"payload.issue.user.login":1,"payload.issue.comments":1})

![screenshot](http://i.imgur.com/EJl5OEG.png)


## Challenge 2 (8 points x 2 = 16 points) 

### 1 (8 points)

How many issues and push events have I personally contributed to?

> db.course_events.find({"type":"PushEvent"},{"actor.login":"dano8957"}).count()
> db.course_events.find({"type":"IssuesEvent"},{"actor.login":"dano8957"}).count()

![screenshot](http://i.imgur.com/0LPfF97.png)

### 2 (8 points)

Who was the first person to create an issue?

> db.course_events.find({'type':'IssuesEvent'},{'actor.login':1,'created_at':1})


![screenshot](http://i.imgur.com/r77gD2D.png)
