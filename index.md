---
layout: default
title: Student Blog
---
<style>
  p{font-family: sans-serif;}
  hr{background-color: blue}
  .color{color: #8EE3F0;}
  body {
    padding: 25px;
    background-color: #8ee3f0;
    color: #1f973b;
    font-size: 16px;
    transition-duration: 0.2s;
  }
  hr{background-color:blue }
  .board {
      display: grid;
      grid-template-columns: repeat(3, 100px);
      grid-gap: 2px;
    }
    .cell {
      width: 100px;
      height: 100px;
      border: 1px solid blue;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 24px;
      cursor: pointer;
    }
</style>
<script>
  
var IsLoggedIn1 = "true";
function myFunction() {
  var element = document.body;
  element.classList.toggle("dark-mode");
  var elem = document.querySelectorAll("#border");
  elem.forEach(function(border) {
    border.classList.toggle("border-dark");
    });
  var bars = document.querySelectorAll("#bar");
  bars.forEach(function(bar) {
    bar.classList.toggle("bar-dark");
    });
  var cellz = document.querySelectorAll("#cells");
  cellz.forEach(function(cells) {
    cells.classList.toggle("cell");
    cells.classList.toggle("cells-dark");
    });
}
</script>
## Gurshawn's Page
![AboutMe](images/CSPAboutME.png)
<head>About Me:</head>
<p>I am a fourteen year old sophmore who wants to learn more about computer science. I was born and raised in San Diego, but my parents are from Punjab.</p>
<head>Favorite Food:</head>
![FavoriteFood](images/download.jpeg)
<ul>
## Overview of Hacks, Study and Tangibles
<p>1. make sure everything is working after each step.
   2. make sure all progmrams are updated
   3. get help from others who have encountered similair problems
   4. You have to use your github url to be able to commit. If you just clone the teacher sample you can only make changes onto  a local host. 
</p>
<p>
  Errors:
  Commit didn't work: The problem was that I had originally been using a git clone of the teacher repository rather than my own. Later the problem was that I was typing in wrong index file, so the commit wasn't recognized.  
  Image didn't work: When entering the picture, I learned I have to use the full file path, so the computer knows where to pull from. 
  Make command failed: The reason my make command didn't work was because some of the files I had downloaded were corrupted.
</p>
<p>While I was setting up my enviornment for class I encountered many problems. Often times when I didn’t understand a command or where to locate a file or folder, I was able to rely on my teammates to explain it to me. Edwin was very helpful.</p>
</ul>
<label>Trimester 1</label>
<table>
<tr>
<th>Period</th><th>Class</th>
</tr>
<tr>
<th>One</th><th>AP Calculus AB</th>
</tr>
<tr>
<th>Two</th><th>AP Chemistry</th>
</tr>
<tr>
<th>Three</th><th>World History 1</th>
</tr>
<tr>
<th>Four</th><th>High School English 3</th>
</tr>
<tr>
<th>Five</th><th>AP Computer Science Principles</th>
</tr>
</table>

- Plans, Lists, [Scrum Boards](https://clickup.com/blog/scrum-board/) help you to track key events, show progress and record time.  Effort is a big part of your class grade.  Show plans and time spent!
- [Hacks(Todo)](https://levelup.gitconnected.com/six-ultimate-daily-hacks-for-every-programmer-60f5f10feae) enable you to stay in focus with key requirements of the class.  Each Hack will produce Tangibles.
- Tangibles or [Tangible Artifacts](https://en.wikipedia.org/wiki/Artifact_(software_development)) are things you accumulate as a learner and coder. 
