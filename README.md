# Basic Networking Example
A barebones example of how to set up a basic networking/multiplayer web app

# What does it do?

Anyone who opens the page can hold down the mouse and move the ball on screen. Anyone else can see the ball moving. 

# How do I run it (on my computer) ?

* Download this repository
* Make sure you have [Node.js](https://nodejs.org/en/) installed. 
* Run this command to install the dependencies (you only need to do this once):
```sh
$ npm install
```
* Run this command to start it up:
```sh
$ node basic_networking.js
```
* Open localhost:8080 in your local browser to see it work! (Try opening multiple tabs and see how they connect!)

# How does it work?

It uses [Socket.io](http://socket.io/) as the networking library.

The server code is in basic_networking.js. All it does is start accepting connections, and whenever it recieves a "new-click" event, it sends it to everyone else who's connected.

The client code is in index.html. All it does is wait to recieve a "new-click" event. When it does, it draws the ball there. When you click, it sends a server a "new-click" event with the x and y of that click.