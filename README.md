# QR-Genertor
# Lets generate the QR using HTML CSS AND JAVASCRIPT
# First HTML CSS

<!DOCTYPE html>
<html lang="en">
<head>
        
    <meta charset="UTF-8">
        
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
        
    <title>QR Code Generator</title>
        
    <script src="https://cdn.jsdelivr.net/npm/qrcode@1.5.1/build/qrcode.min.js"></script>
        
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 0 auto;
            padding: 20px;
            text-align: center;
        }
        #qr-code {
            margin: 20px auto;
        }
        input, button {
            padding: 10px;
            width: 100%;
            margin: 10px 0;
        }
        button {
            background: #007bff;
            color: white;
            border: none;
            cursor: pointer;
        }
   </style>
</head>
  
  # Now, using JAVESCRIPT   
  
  <body>
        
    <h1>QR Code Generator</h1>
        
    <input type="text" id="qr-input" placeholder="Enter text or URL">
    <button onclick="generateQR()">Generate QR Code</button>
    <div id="qr-code"></div>

    <script>
        function generateQR() {
            const input = document.getElementById("qr-input").value;
            if (!input) {
                alert("Please enter text or URL!");
                return;
            }

            // Clear previous QR code
            document.getElementById("qr-code").innerHTML = "";

            // Generate new QR code
            new QRCode(document.getElementById("qr-code"), {
                text: input,
                width: 200,
                height: 200,
                colorDark: "#000000",
                colorLight: "#ffffff",
                correctLevel: QRCode.CorrectLevel.H
            });
        }
    </script>
</body>
</html>
