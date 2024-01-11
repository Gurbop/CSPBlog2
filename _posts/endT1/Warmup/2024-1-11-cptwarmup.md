---
toc: true
comments: false
layout: post
title: Text to Color Converter
type: tangibles
courses: { compsci: {week: 15} }
---
<html>
<head>
  <style>
    #colorDisplay {
      width: 500px;
      height: 100px;
      border: 1px solid #000;
      margin-left: 500px;
      margin-bottom: 10px;
    }
    #container {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
    }
    button,
    label[for="fileInput"] {
      display: inline-block;
      padding: 8px 12px;
      font-size: 14px;
      background-color: #007bff;
      color: #fff;
      cursor: pointer;
      border: none;
      border-radius: 4px;
      margin-right: 10px;
    }
  </style>
</head>
<body>
  <div id="container">
    <input type="text" id="textInput" placeholder="Enter text">
    <input type="text" id="textOutput" placeholder="Converted text" readonly>
    <input type="text" id="imageBinaryOutput" placeholder="Image Binary" readonly>
    <button onclick="convertText()">Convert Text</button>
  </div>
  <div id="canvasContainer">
    <div id="colorDisplay"></div>
    <button id="downloadBtn" onclick="downloadImage()">Download Image</button>
    <label for="fileInput">Upload Image</label>
    <input type="file" id="fileInput" onchange="convertImageToBinary(event)" style="display: none;">
    <button id="convertToTextBtn" onclick="convertImageToText()">Convert Image to Text</button>
  </div>

  <script>
    function textToBinary(text) {
      let binary = '';
      for (let i = 0; i < text.length; i++) {
        let charBinary = text[i].charCodeAt(0).toString(2);
        while (charBinary.length < 8) {
          charBinary = '0' + charBinary;
        }
        binary += charBinary;
      }
      return binary;
    }

    function binaryToRGB(binary) {
      let rgbValues = [];
      for (let i = 0; i < binary.length; i += 24) {
        let r = parseInt(binary.substring(i, i + 8), 2);
        let g = parseInt(binary.substring(i + 8, i + 16), 2);
        let b = parseInt(binary.substring(i + 16, i + 24), 2);
        if (!(r === 0 && g === 0 && b === 0)) {
          rgbValues.push([r, g, b]);
        }
      }
      return rgbValues;
    }

    function displayColor(rgbValues) {
      const canvas = document.createElement('canvas');
      canvas.width = rgbValues.length * 10;
      canvas.height = 50;
      const c = canvas.getContext('2d');
      for (let i = 0; i < rgbValues.length; i++) {
        c.fillStyle = `rgb(${rgbValues[i][0]}, ${rgbValues[i][1]}, ${rgbValues[i][2]})`;
        c.fillRect(i * 10, 0, 10, 50);
      }
      const colorDisplay = document.getElementById('colorDisplay');
      colorDisplay.innerHTML = '';
      colorDisplay.appendChild(canvas);
    }

    function convertText() {
      const inputText = document.getElementById('textInput').value;
      const binaryText = textToBinary(inputText);
      const rgbValues = binaryToRGB(binaryText);
      displayColor(rgbValues);
    }

    function downloadImage() {
      const canvas = document.querySelector('canvas');
      const dataURL = canvas.toDataURL();
      const a = document.createElement('a');
      a.href = dataURL;
      a.download = 'color_image.png';
      a.click();
    }

    function convertImageToBinary(event) {
      const file = event.target.files[0];
      const reader = new FileReader();
      reader.onload = function (e) {
        const image = new Image();
        image.onload = function () {
          const canvas = document.createElement('canvas');
          canvas.width = image.width;
          canvas.height = image.height;
          const ctx = canvas.getContext('2d');
          ctx.drawImage(image, 0, 0);
          const imageData = ctx.getImageData(0, 0, canvas.width, canvas.height).data;

          let binaryString = '';
          for (let i = 0; i < imageData.length; i += 4) {
            const r = imageData[i];
            const g = imageData[i + 1];
            const b = imageData[i + 2];

            if (!(r === 0 && g === 0 && b === 0)) {
              binaryString += ('00000000' + r.toString(2)).slice(-8);
              binaryString += ('00000000' + g.toString(2)).slice(-8);
              binaryString += ('00000000' + b.toString(2)).slice(-8);
            }
          }

          document.getElementById('textInput').value = binaryString;
          document.getElementById('imageBinaryOutput').value = binaryString;
        };
        image.src = e.target.result;
      };
      reader.readAsDataURL(file);
    }

    function convertImageToText() {
      const binaryString = document.getElementById('textInput').value;
      let text = '';
      let skipBlack = false;
      let uniqueColors = new Set();

      for (let i = 0; i < binaryString.length; i += 24) {
        const r = parseInt(binaryString.substring(i, i + 8), 2);
        const g = parseInt(binaryString.substring(i + 8, i + 16), 2);
        const b = parseInt(binaryString.substring(i + 16, i + 24), 2);

        if (r === 0 && g === 0 && b === 0) {
          skipBlack = true;
        } else {
          if (!skipBlack) {
            const colorKey = `${r}${g}${b}`;
            if (!uniqueColors.has(colorKey)) {
              text += String.fromCharCode(r) + String.fromCharCode(g) + String.fromCharCode(b);
              uniqueColors.add(colorKey);
            }
          }
          skipBlack = false;
        }
      }
      let convertedText = '';
      for (let i = 0; i < text.length; i += 3) {
        convertedText += text.substring(i, i + 3) + ' ';
      }
      document.getElementById('textOutput').value = convertedText.trim();
    }
  </script>
</body>
</html>
