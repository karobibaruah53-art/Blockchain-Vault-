<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Verification Page</title>
    <style>
        body { font-family: Arial, sans-serif; background: #f0f0f0; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; }
        .container { background: white; padding: 40px; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); text-align: center; max-width: 400px; }
        h1 { color: #333; }
        p { color: #666; }
        input { padding: 10px; width: 100px; margin: 20px 0; }
        button { padding: 10px 20px; background: #007bff; color: white; border: none; cursor: pointer; }
        button:hover { background: #0056b3; }
        #message { margin-top: 20px; font-weight: bold; }
    </style>
</head>
<body>
    <div class="container">
        <h1>My Secure Protocol</h1>
        <p>Complete the security verification to continue:</p>
        <p id="mathProblem"></p>
        <input type="number" id="userAnswer" placeholder="Your answer">
        <br>
        <button onclick="checkAnswer()">Verify & Continue</button>
        <div id="message"></div>
    </div>

    <script>
        let num1, num2, correctAnswer;

        function generateMath() {
            num1 = Math.floor(Math.random() * 20) + 1;
            num2 = Math.floor(Math.random() * 20) + 1;
            correctAnswer = num1 + num2;
            document.getElementById('mathProblem').textContent = `\( {num1} + \){num2} = ?`;
            document.getElementById('message').textContent = '';
            document.getElementById('userAnswer').value = '';
        }

        function checkAnswer() {
            const userInput = parseInt(document.getElementById('userAnswer').value);
            if (userInput === correctAnswer) {
                document.getElementById('message').textContent = 'Verified! You may proceed.';
                document.getElementById('message').style.color = 'green';
                // Here you could redirect: window.location.href = 'next-page.html';
            } else {
                document.getElementById('message').textContent = 'Incorrect. Try again.';
                document.getElementById('message').style.color = 'red';
                generateMath();
            }
        }

        // Generate first problem on load
        generateMath();
    </script>
</body>
</html>
