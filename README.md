<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Breteau Index Result</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; }
        .container { max-width: 600px; margin: auto; padding: 20px; }
        img, iframe { width: 100%; max-width: 600px; margin-top: 20px; }
        .warning { font-size: 18px; font-weight: bold; color: red; margin-top: 20px; }
    </style>
</head>
<body>
    <div class="container">
        <h1>Breteau Index Result</h1>
        <h2>Your Breteau Index is: <span id="result"></span></h2>
        <p id="warning" class="warning"></p>
        
        <h3>Map of Nallur Area, Jaffna</h3>
        <img src="image.png" alt="Map of Nallur Area, Jaffna">
        
        <h3>Dengue Prevention Video</h3>
        <iframe width="560" height="315" src="https://www.youtube.com/embed/Fixp7OAYFfA" frameborder="0" allowfullscreen></iframe>
        
        <br><br>
        <button onclick="goBack()">Calculate Again</button>
    </div>
    
    <script>
        window.onload = function() {
            // Retrieve the Breteau Index from localStorage
            let index = parseFloat(localStorage.getItem('breteauIndex')) || 0;
            document.getElementById('result').innerText = index + '%';  // Display the result
            
            // Warning messages based on the index value
            let warningText = "";
            if (index > 50) {
                warningText = "EVACUATE TEMPORARILY AND ONLY MOVE IN AFTER ACTIONS BY YOUR LOCAL AUTHORITY AND ORGANIZATIONS. FOLLOW ALL HEALTH ADVICE.";
            } else if (index > 20) {
                warningText = "CAUTION - DANGEROUS DENGUE BREEDING GROUNDS. Contact local authorities immediately.";
            }
            document.getElementById('warning').innerText = warningText;
        };

        // Go back to index.html for new calculations
        function goBack() {
            window.location.href = 'index.html';
        }
    </script>
</body>
</html>

