<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pastel Q&A</title>
    <style>
        /* 🌸 Page Styling */
        body {
            background: linear-gradient(to bottom, #FFD1DC, #FFF5BA);
            font-family: "Papyrus", sans-serif;
            text-align: center;
            padding: 50px;
            color: #5A3E36;
        }

        /* 🌸 Main Container */
        .container {
            background: #FFEEF0;
            padding: 50px;
            border: 2px solid #FFB6C1;
            border-radius: 20px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            display: flex;
            flex-direction: column;
            align-items: center; /* 🌟 Ensures content is centered */
            justify-content: center;
            width: 60%;
            max-width: 600px; /* 🌟 Prevents it from getting too wide */
            margin: 20px auto; /* 🌟 Centers the form on the page */
        }

        /* 🌸 Question Title */
        h1 {
            font-size: 22px;
            margin-bottom: 20px;
        }

        /* 🌸 Answer Input Box */
        input {
            width: 80%;
            height: 40px;
            padding: 10px;
            border: 2px solid #FFB6C1;
            border-radius: 10px;
            font-size: 16px;
        }

        /* 🌸 Submit Button */
        .submit-btn {
            background: #e0b6cf;
            color: #5A3E36;
            padding: 12px 25px;
            border: 2px solid #FFB6C1;
            border-radius: 10px;
            cursor: pointer;
            font-size: 18px;
            margin-top: 20px;
            display: block;
            text-align: center;
        }

        /* 🌟 Center the Submit Button Properly */
        .submit-container {
            display: flex;
            justify-content: center; /* 🌟 Centers the button */
            margin-top: 20px;
        }

        /* 🌸 Decorative Images */
        .strawberry {
            position: absolute;
            top: 10px;
            left: 10px;
            width: 150px;
        }
        
        .duck {
            position: fixed;
            bottom: 10px;
            right: 10px;
            width: 100px;
        }

        /* 🌸 Credits Section */
        .credits {
            margin-top: 40px;
            font-size: 14px;
            color: #5A3E36;
        }
        .credits ul {
            list-style: none;
            padding: 0;
        }
        .credits li {
            margin-bottom: 5px;
        }

        /* 🌸 Copyright */
        .copyright {
            margin-top: 20px;
            font-size: 12px;
            color: #5A3E36;
        }

        /* 🌟 Responsive Design with Media Queries */

        /* For tablets (≤ 768px) */
        @media (max-width: 768px) {
            .container {
                width: 80%;  /* Adjust width */
                padding: 30px;
            }
            h1 {
                font-size: 20px;
            }
            input {
                font-size: 14px;
                width: 90%;
            }
            .submit-btn {
                width: 80%; /* 🌟 Makes button adapt to smaller screens */
            }
            .strawberry {
                width: 120px;
            }
            .duck {
                width: 80px;
            }
        }

        /* For mobile screens (≤ 480px) */
        @media (max-width: 480px) {
            .container {
                width: 95%;  /* Full width */
                padding: 20px;
            }
            h1 {
                font-size: 18px;
            }
            input {
                font-size: 14px;
                width: 100%;  /* Full width */
            }
            .submit-btn {
                width: 100%; /* 🌟 Full-width button on small screens */
            }
            .strawberry {
                width: 80px;
                top: 5px;
                left: 5px;
            }
            .duck {
                width: 60px;
                bottom: 5px;
                right: 5px;
            }
        }
    </style>
</head>
<body>

    <!-- 🌸 Decorative Images -->
    <img src="https://assets.onecompiler.app/43ab3rkmv/43ab3taem/strawberry%20(1).png" alt="Strawberry" class="strawberry">
    <img src="https://assets.onecompiler.app/43ab3rkmv/43ab3taem/duck.png" alt="Duck" class="duck">

    <!-- 🌸 Form (All questions in one form) -->
    <form action="https://docs.google.com/forms/d/e/1FAIpQLSfTybyWbnYvin_S8t04Dh47xfsLvIe1jva3yZ8vV_W9p6VNnw/formResponse" method="GET" target="_blank">
        <div class="container">
            <h1>What is your name?</h1>
            <input type="text" name="entry.594710907" placeholder="Write your name here..." required>
        </div>

        <div class="container">
            <h1>What is your favourite song?</h1>
            <input type="text" name="entry.2089872087" placeholder="Write name or paste link..." required>
        </div>

        <div class="container">
            <h1>What is that one song you always listen to when you're sad?</h1>
            <input type="text" name="entry.686509013" placeholder="Write name or paste link..." required>
        </div>

        <!-- 🌟 Submit Button (Now properly centered) -->
        <div class="submit-container">
            <button type="submit" class="submit-btn">Submit</button>
        </div>
    </form>

    <!-- 🌸 Credits Section -->
    <div class="credits">
        <p><strong>Image Credits:</strong></p>
        <ul>
            <li>Strawberry PNG by <a href="https://www.flaticon.com/free-icons/food" target="_blank">smashingstocks - Flaticon</a></li>
            <li>Strawberry-blossoms PNG by <a href="https://assets.onecompiler.app/43ab3rkmv/43ab3taem/strawberry-blossoms.png" target="_blank">Freepik - Flaticon</a></li>
        </ul>
    </div>

    <!-- 🌸 Copyright -->
    <div class="copyright">
        © 2025 by Camellia Banerjee
    </div>

</body>
</html>

       

 
