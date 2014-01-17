# The Estimate-o-Meter

## Learning Meteor.js by Building a Planning Poker App.

### This needs a better name, I've already written ""beverage-o-meter" several times on accedent.

////

# An Unexpected Journey

* ### Inspired by last years unConf, going to learn moble app developemnt
* ### Made "hello world" for Android.
* ### "An API for planning poker would be easy to write."
* ### Python and Google's App Engine.
* ### Websockets.
* ### Node.js

////

![Meteor JS](https://raw.github.com/jachin/cw-unconf-estimate-o-meter/master/meteorjs.jpg)

////
 
# Meteor is great...

 * ### Lots of good resouces for learning.
 * ### Javascript everwhere and that's actually fun.
 * ### Real time, out of the box, always.
 * ### Lots of Pakages. It can use a lot of the Node.js stuff.
 * ### Magic. It works and you don't feel like you've done anything.

////

# Unexpected Education

 * ### MongoDB
 * ### Bootsrap 3
 * ### Nginx
 * ### underscore.js
 * ### Javascript

////

# Unexpected Difficulties

* ### New Framework. Life on the edge.
* ### Paradigm Shift (for me anyway).
* ### A real time Planning Poker app is complicated.

////

# Magic You Say?

* ### Distributed Data Protocol (DDP)
* ### Remote Procedure Calls (RPC)
* ### Reactivity (like AngularJS)
* ### Latency compensation.

////

# Getting Started
## In just 2 minutes (or less).

`https://www.meteor.com`

`curl https://install.meteor.com/ | sh`

`cd ~/Desktop`

`meteor create sampleApp`

`cd sampleApp`

`meteor`

////

# Watch the Meteor Videos

* ### 20 minutes of video.
* ### Try the sample projects.
* ### Super easy to get started
* ### Deploy right on meteor.com

////

# Code: Projects

```javascript
// Get the user ID.
Meteor.userId();

// Find all the projects.
Projects.find().fetch();

// Add a project.
var projectId = Projects.insert({
	name: 'This is a test project.',
	timestamp: (new Date()).getTime(),
	owner: Meteor.userId()
});

// Edit a project's name
Projects.update(projectId, {$set: {name: value}});

// Remove a project
Projects.remove(projectId);
```

////

# Unit Tests?

## You bet.

	meteor test-packages

////

# "Production" Stack

* ### Ubuntu
* ### MongoDB
* ### nginx
* ### Node.js

////

# Deployment (part 1)

Bundle up the app.

    meteor bundle eom.tar.gz

Upload to server

stop meteor with forever

    cd /usr/share/nginx/eom.atili.us/bundle
    forever stop main.js

remove the old files

    cd /usr/share/nginx/eom.atili.us
    rm -R bundle

Extract:

    tar -xzf ~/eom.tar.gz -C /usr/share/nginx/eom.atili.us

Go to the directory

    cd /usr/share/nginx/eom.atili.us/bundle        
    
////

# Deployment (part 2)

Clean up fibers:

	rm -r programs/server/node_modules/fibers

Install fibers:

	npm install fibers@1.0.1

load environment:

	source ../eom_env.sh

restart node with forever

	forever start main.js

////

# Demo

## Lets estimate a project.

### https://eom.atili.us

////

# Is the Estimate-o-meter ready?

////

# It's Kinda Ready

* ### CSV download of finished results
* ### Unit tests
* ### A real domain name an ssl cert.
* ### Better name?
* ### Lots of "smaller" features.
* ### It could looks better.

////

# Big Features (the Future)

* ### Non-simultaneous estimating.
* ### Mobile App. Phone Gap.
* ### More features for "Scrum" and "Agile".

////

# Is Meteor Right For...?

* ### Building a prototype? *YES!*
* ### If I don't want to use MongoDB? *No! Maybe someday.*
* ### If I don't want to host a Node.js app? *No!*
* ### app needs to be real time? *Maybe. You should really consider it.*
* ### I require a battle tested stable enviornment? *No! Maybe someday.*
* ### But what if I'm asking these questions in the future? *1.0 first quarter 2014.*

////

# Questions/Discussion

////

# Thank You.

## May your estimates always be just a tiny bit to big.
