---
toc: true
comments: false
layout: post
title: Calculator
description: This is a calculator.
type: hacks
courses: { compsci: {week: 1} }
---
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