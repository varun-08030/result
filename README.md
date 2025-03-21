<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tap to Reveal Results</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
            padding: 20px;
        }
        .container {
            max-width: 400px;
            margin: auto;
        }
        .name-box {
            background-color: #007BFF;
            color: white;
            padding: 15px;
            margin: 10px;
            cursor: pointer;
            border-radius: 8px;
            font-size: 18px;
        }
        .result {
            display: none;
            margin-top: 10px;
            padding: 10px;
            background-color: white;
            border: 2px solid #007BFF;
            border-radius: 8px;
        }
    </style>
</head>
<body>

    <h2>Tap to Reveal Your Test Result</h2>
    <div class="container">
        <div class="name-box" onclick="showResult('result1')">John Doe</div>
        <div id="result1" class="result">Score: 85/100 - Great Job! 🎉</div>

        <div class="name-box" onclick="showResult('result2')">Jane Smith</div>
        <div id="result2" class="result">Score: 72/100 - Good Work! 👍</div>

        <div class="name-box" onclick="showResult('result3')">Alex Brown</div>
        <div id="result3" class="result">Score: 90/100 - Excellent! 🏆</div>
    </div>

    <script>
        function showResult(id) {
            var resultDiv = document.getElementById(id);
            if (resultDiv.style.display === "none" || resultDiv.style.display === "") {
                resultDiv.style.display = "block";
            } else {
                resultDiv.style.display = "none";
            }
        }
    </script>

</body>
</html>
