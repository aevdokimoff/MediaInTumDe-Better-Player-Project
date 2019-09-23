# grnvs-local-vid-server-project

## About
Hi! This is the Media.in.tum.de-Local-Vid-Server Project made for TUM Informatics students, who wants to watch any lecture recording on [https://media.net.in.tum.de](https://media.net.in.tum.de) web site (e.g. GRNVS lectures), but faces the inability to view them due to the inoperability of the player when trying to play back camera and slides simultaneously. 

## Usage
* Go to [https://media.net.in.tum.de](https://media.net.in.tum.de) in your browser and open the lecture you want to watch (you may try to reload the page a couple of times if it won't load the player on the media.net.in.tum.de website). 
* Log in with your TUM ID
* Start localhost on your PC and put the projects files (or just index.html) to your localhost root directory.  
*(You can use [Web Server for Chrome](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb) Extension)*
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
(`http://127.0.0.1:8887` is your localhost address and port)
* The page with two videos side by side will open. Press `play` and enjoy the lecture

## P.S.

Feel free to use this tool and be happy with the lectures 👍

Made by Artem Evdokimov, TUM, B.Sc. Informatics  
[aevdokimoff.github.io](http://aevdokimoff.github.io)
