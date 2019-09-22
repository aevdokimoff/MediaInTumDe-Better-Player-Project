# grnvs-local-vid-server-project
grnvs-local-vid-server-project

## About
Hi! This is GRNVS-Local-Vid-Server Project made for TUM Informatics students, who wants to watch the GRNVS lectures, but faces the inability to view them due to the inoperability of the player when playing two videos simultaneously. 

## Usage
* Open [https://media.net.in.tum.de](https://media.net.in.tum.de) in your browser (you may try to reload the page a couple of times if it won't load the player on the media.net.in.tum.de website). 
* Start localhost on your PC and put the projects files (or just index.html) to your localhost root directory.  
*You can use [Web Server for Chrome](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb) Extension*
* Open Console of your browser (for Chrome: `Command + Option + J` on macOS and `Control + Shift + J` on Windows)
* Type the following code and press Enter:
```
(function () { 'use strict'; if (!confirm('Get?')) return; 
var cameraLink = document.body.querySelectorAll('a.vtip[title^="camera.mp4"]'); 
var slidesLink = document.body.querySelectorAll('a.vtip[title^="slides.mp4"]'); 
var url = 'http://127.0.0.1:8887?' + cameraLink[0].href + '#' + slidesLink[0].href;
window.open(url, '_blank');
}());
```
* The page with two videos side by side will open. Press `play` and enjoy the lecture
