---
toc: true
comments: false
layout: post
title: Tic Tac Toe
description: This is the Tic Tac Toe game.
type: hacks
courses: { compsci: {week: 1} }
---
<html>
    
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
    <body>
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