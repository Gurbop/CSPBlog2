---
layout: post
title: Web Programming eview Ticket
description: An introduction to key topics in Web Programming self-graded rubric.
courses: {compsci: {week: 6} }
type: tangibles
---
<p>Errors:</p>
<p>code not working because we didn't switch the cell to python, pages not found because the permalink was modified</p>
<p>Rubric:</p>
<p>.5: Have a working HTML code cell in a notebook based on the wireframe representation provided under HTML hacks (HTML Hack)</p>
<p>.5: Have a working javascript code cell in a notebook which creates, manipulates, and logs an object (Data Types Hack)</p>
<p>.5: Have a working javascript code cell in a notebook which creates, manipulates, and logs an object (Data Types Hack)</p>
<p>.5:Have a working javascript code cell in a notebook which compares two variables (Javascript Hack)</p>
<p>.5:Have code cells in a notebook which shows the corrections made to the first three code cells in the 1.4 correcting errors page (Correcting Errors Hack)</p>

<p>For the basics of js, we first created 2 variables, and used the prompt function to get user input. Then using if statements we wer able to compare the numerical values and using console.log we were able to log which variable had the greater value.</p>
<p>HTML:
I decided to follow the hacks, but experiment with different links with the href attribute, but explore further by developing a dark mode button that toggles the dark mode of the webpage. 
I experimented with css to make the button look nicer, also to change the color of text, make a hover animation and so on.
I stole the base code from header.html, in order to make my dark mode button appear on every webpage.
Errors:
The css for changing the background didn’t work very well originally, since it only changed the css of 1 element, fixed by adding ids to elements that I want to change, then writing a Javascript script to toggle the css class of all elements with the given ID.


JS Debugging:
I decided to follow the hacks, but for the last hack, I tried to implement input from a text box.
Fixed all 3 code cells with the correct functionality

Errors:
Jupyter Notebook not running the JS code, investigate adding new kernels in the future
I had a couple problems with JS syntax, such as forgetting the semicolon
For the first code cell, had an error where it only displayed numbers up until 99, but fixed by making i > 101
</p>
<p>Message Switcher 

Introduction
The "Message Switcher" is a simple yet visually engaging web page that demonstrates the use of HTML, CSS, and JavaScript to dynamically switch messages when a button is clicked. The page includes a button and a paragraph with an initial message, and it utilizes basic styling and animations to make the experience more appealing.

HTML Structure
The HTML structure of the page is minimal, comprising essential elements:

<button> element with the ID "switchButton": This button triggers the message switching action.

<p> element with the ID "status": This paragraph initially displays the message "Not Switched" and will be dynamically updated with new messages.

JavaScript Functionality
The JavaScript code adds interactivity to the web page:

Function switchMessage: This function is called when the "Switch Message" button is clicked. It performs the following tasks:

Defines an array of positive messages like "Nice Switching!", "Not Very Useful!", "Funni Prank!", and "Why did I make this!".

Randomly selects a new message from the array that is different from the current message.
Applies the "switchAnimation" to animate the message switching.
Updates the "status" paragraph with the new message.
Button Event Listener: An event listener is added to the "switchButton" element. When the button is clicked, it triggers the switchMessage function, resulting in the dynamic message switch (DOM). 

User Experience
When a user visits this web page and clicks the "Switch Message" button, they experience an engaging transition. The message is not only changed but also animated with a scaling and fade-in/fade-out effect, making the message switch visually appealing.

This simple yet effective demonstration showcases the power of HTML, CSS, and JavaScript to create interactive and engaging web pages. The "Message Switcher" can serve as a starting point for more complex web applications or as an interesting addition to any website.
</p>
<p>Data Types: The project consisted of creating an object with attributes name, age, classes, interests, favorite_songs, id_num, num_games, and num_wins. The number of games and wins is considering our plan for the passion project, a game (considering connect 4) that also supports chatting. For the attributes, I added an array for my interests in order to show a list of interests instead of a single one. Same thing for favorite_songs. The id_num is for verifying an account because we are planning on creating a database for users. This will keep track of the number of games as well as the number of wins. I have also added a calculation code that calculates the total win percentage.

Errors
Tried to implement classes into JS but always resulted in error.
The classes weren't working but the objects were.
DOM:
Message Switcher

Introduction
The "Message Switcher" is a simple yet visually engaging web page that demonstrates the use of HTML, CSS, and JavaScript to dynamically switch messages when a button is clicked. The page includes a button and a paragraph with an initial message, and it utilizes basic styling and animations to make the experience more appealing.
HTML Structure
The HTML structure of the page is minimal, comprising essential elements:
element with the ID "switchButton": This button triggers the message switching action.
element with the ID "status": This paragraph initially displays the message "Not Switched" and will be dynamically updated with new messages - JavaScript Functionality The JavaScript code adds interactivity to the web page: Function switchMessage: This function is called when the "Switch Message" button is clicked. It performs the following tasks: Defines an array of positive messages like "Nice Switching!", "Not Very Useful!", "Funni Prank!", and "Why did I make this!". Randomly selects a new message from the array that is different from the current message. Applies the "switchAnimation" to animate the message switching. Updates the "status" paragraph with the new message. Button Event Listener: An event listener is added to the "switchButton" element. When the button is clicked, it triggers the switchMessage function, resulting in the dynamic message switch (DOM). - User Experience When a user visits this web page and clicks the "Switch Message" button, they experience an engaging transition. The message is not only changed but also animated with a scaling and fade-in/fade-out effect, making the message switch visually appealing. This simple yet effective demonstration showcases the power of HTML, CSS, and JavaScript to create interactive and engaging web pages. The "Message Switcher" can serve as a starting point for more complex web applications or as an interesting addition to any website.

Javascript:
We added a function that takes in two arguments. These will be the score of one player and the score of another. This is for our later project where we will have a scoring system where the player with the highest score wins. The Tic Tac Toe game is a simpler version for the future connect 4 game. This is because we have user interaction where it also has a simple visual representation. This code doesn't contain any actual visual attributes but for the passion project, we want to create a custom interface. Also, the tic tac toe uses similar logic to the one of connect 4, therefore it is a good way of preparing for the passion project.

HTML:
I decided to follow the hacks, but experiment with different links with the href attribute, but explore further by developing a dark mode button that toggles the dark mode of the webpage.
I experimented with css to make the button look nicer, also to change the color of text, make a hover animation and so on.
I stole the base code from header.html, in order to make my dark mode button appear on every webpage.
The Tic Tac Toe game is a simpler version for the future connect 4 game. This is because we have user interaction where it also has a simple visual representation. This code doesn't contain any actual visual attributes but for the passion project, we want to create a custom interface. Also, the tic tac toe uses similar logic to the one of connect 4, therefore it is a good way of preparing for the passion project.

Errors:
The css for changing the background didn’t work very well originally, since it only changed the css of 1 element, fixed by adding ids to elements that I want to change, then writing a Javascript script to toggle the css class of all elements with the given ID.
JS Debugging:
I decided to follow the hacks, but for the last hack, I tried to implement input from a text box.
Fixed all 3 code cells with the correct functionality

Errors:
Jupyter Notebook not running the JS code, investigate adding new kernels in the future
I had a couple problems with JS syntax, such as forgetting the semicolon
For the first code cell, had an error where it only displayed numbers up until 99, but fixed by making i > 101</p>