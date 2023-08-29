---
layout: default
title: Student Blog
---
<style>
  backgroud-color: solid blue;
</style>
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
<p>While I was setting up my enviornment for class I encountered many problems. Often times when I didn’t understand a command or where to locate a file or folder, I was able to rely on my teammates to explain it to me.</p>
</ul>

<p>Calculator</p>
<div id="calculator">
    <div style="max-width: 200px; background-color: #3b6fd1; padding: 20px; max-hieght: 1000px;">
      <input type="text" id="display" disabled="" />
      <br />
      <button onclick="appendToDisplay('1')">1</button>
      <button onclick="appendToDisplay('2')">2</button>
      <button onclick="appendToDisplay('3')">3</button>
      <button onclick="appendToDisplay('*')">x</button>
      <button onclick="appendToDisplay('+')">+</button>
      <button onclick="appendToDisplay('-')">-</button>
      <br />
      <button onclick="appendToDisplay('4')">4</button>
      <button onclick="appendToDisplay('5')">5</button>
      <button onclick="appendToDisplay('6')">6</button>
      <button onclick="calculate()">=</button>
      <button onclick="appendToDisplay('/')">/</button>
      <button onclick="clearDisplay()">C</button>
      <br />
      <button onclick="appendToDisplay('7')">7</button>
      <button onclick="appendToDisplay('8')">8</button>
      <button onclick="appendToDisplay('9')">9</button>
      <br />
      <button onclick="appendToDisplay('0')">0</button>
    
    </div>
    
    <script>
      let display = document.getElementById('display');
    
      function appendToDisplay(value) {
        display.value += value;
      }
    
      function calculate() {
        try {
          display.value = eval(display.value);
        } catch (error) {
          display.value = 'Error';
        }
      }
    
      function clearDisplay() {
        display.value = '';
      }
    </script>
  
    
    <head>
      <br />
      <h1 span="" style="color: green; font-size: 20px;">Tic Tac Toe </h1>
      <style>
        .board {
          display: grid;
          grid-template-columns: repeat(3, 100px);
          grid-gap: 1px;
        }
        .cell {
          width: 100px;
          height: 100px;
          border: 1px solid green;
          display: flex;
          align-items: center;
          justify-content: center;
          font-size: 24px;
          cursor: pointer;
        }
      </style>
    </head>
    <body>
      <div class="board" id="board">
        <div class="cell"></div>
        <div class="cell"></div>
        <div class="cell"></div>
        <div class="cell"></div>
        <div class="cell"></div>
        <div class="cell"></div>
        <div class="cell"></div>
        <div class="cell"></div>
        <div class="cell"></div>
      </div>
    
      <script>
        const board = document.getElementById('board');
        const cells = document.querySelectorAll('.cell');
        let currentPlayer = 'X';
        let gameActive = true;
    
        cells.forEach(cell => {
          cell.addEventListener('click', handleCellClick);
        });
    
        function handleCellClick(event) {
          const clickedCell = event.target;
          const clickedIndex = Array.from(cells).indexOf(clickedCell);
    
          if (gameActive && !cells[clickedIndex].textContent) {
            cells[clickedIndex].textContent = currentPlayer;
            checkWin();
            currentPlayer = currentPlayer === 'X' ? 'O' : 'X';
          }
        }
    
        function checkWin() {
          const winCombinations = [
            [0, 1, 2], [3, 4, 5], [6, 7, 8], 
            [0, 3, 6], [1, 4, 7], [2, 5, 8],
            [0, 4, 8], [2, 4, 6]           
          ];
    
          for (const combination of winCombinations) {
            const [a, b, c] = combination;
            if (cells[a].textContent && cells[a].textContent === cells[b].textContent && cells[a].textContent === cells[c].textContent) {
              gameActive = false;
              alert(`${cells[a].textContent} wins!`);
              clear;
            }
          }
        }
        
      </script>
    </body>


  </div>

- Plans, Lists, [Scrum Boards](https://clickup.com/blog/scrum-board/) help you to track key events, show progress and record time.  Effort is a big part of your class grade.  Show plans and time spent!
- [Hacks(Todo)](https://levelup.gitconnected.com/six-ultimate-daily-hacks-for-every-programmer-60f5f10feae) enable you to stay in focus with key requirements of the class.  Each Hack will produce Tangibles.
- Tangibles or [Tangible Artifacts](https://en.wikipedia.org/wiki/Artifact_(software_development)) are things you accumulate as a learner and coder. 
