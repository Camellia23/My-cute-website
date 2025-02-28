
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Favourite Song</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: linear-gradient(to bottom, #ffd6e0, #ffe5b4);
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 600px;
            margin: 20px auto;
            padding: 20px;
        }
        .question-box {
            background: #ffeef2;
            padding: 20px;
            margin: 20px 0;
            border-radius: 12px;
            box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
        }
        .question-box h3 {
            color: #5a2a27;
            margin-bottom: 10px;
        }
        .input-field {
            width: 90%;
            padding: 10px;
            border: 1px solid #ffb6c1;
            border-radius: 8px;
            outline: none;
            font-size: 16px;
        }
        .submit-btn {
            display: block;
            width: 50%;
            max-width: 200px;
            padding: 10px;
            margin: 20px auto;
            background: #ff9aa2;
            border: none;
            border-radius: 8px;
            font-size: 18px;
            color: white;
            cursor: pointer;
            transition: 0.3s;
        }
        .submit-btn:hover {
            background: #ff6b81;
        }
        @media (max-width: 600px) {
            .question-box {
                padding: 15px;
            }
            .input-field {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <h1>Your Favourite Song</h1>
    <div class="container">
        <div class="question-box">
            <h3>What is your name?</h3>
            <input type="text" class="input-field" placeholder="Write your name here...">
        </div>
        <div class="question-box">
            <h3>What is your favourite song?</h3>
            <input type="text" class="input-field" placeholder="Write name or paste link...">
        </div>
        <div class="question-box">
            <h3>What is that one song you always listen to when you're sad?</h3>
            <input type="text" class="input-field" placeholder="Write name or paste link...">
        </div>
        <button class="submit-btn">Submit</button>
    </div>
</body>
</html>


       

 
