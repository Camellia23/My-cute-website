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
            padding: 20px;
            color: #5A3E36;
            margin: 0;
        }
        /* 🌸 Main Container */
        .container {
            background: #FFEEF0;
            padding: 30px;
            border: 2px solid #FFB6C1;
            border-radius: 20px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            width: 90%;
            max-width: 600px;
            margin: 20px auto;
        }

        /* 🌸 Question Title */
        h1 {
            font-size: 22px;
            margin-bottom: 20px;
        }

        /* 🌸 Answer Input Box */
        input {
            width: 90%;
            max-width: 400px;
            height: 40px;
            padding: 10px;
            border: 2px solid #FFB6C1;
            border-radius: 10px;
            font-size: 16px;
            margin: 0 auto;
            display: block;
        }

        /* 🌸 Submit Button */
        .submit-btn {
            background: #e0b6cf;
            color: #5A3E36;
            padding: 10px 20px;
            border: 2px solid #FFB6C1;
            border-radius: 10px;
            cursor: pointer;
            font-size: 18px;
            margin: 20px auto;
            display: block;
        }
        .submit-btn:hover {
            background: #eb3169;
        }

        /* 🌸 Copyright */
        .copyright {
            margin-top: 20px;
            font-size: 12px;
            color: #5A3E36;
        }

        /* 🌸 Pop-Up Styling */
        .popup {
            display: none; /* Hidden by default */
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: #A2DDF0; /* Pastel blue */
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            font-size: 18px;
            color: #5A3E36;
            z-index: 1000;
        }

        /* 🌸 Overlay Styling */
        .overlay {
            display: none; /* Hidden by default */
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 999;
        }
    </style>
</head>
<body>

    <!-- 🌸 Form (All questions in one form) -->
    <form id="qaForm">
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

        <button type="submit" class="submit-btn">Submit</button>
    </form>

    <!-- 🌸 Pop-Up -->
    <div class="overlay" id="overlay"></div>
    <div class="popup" id="popup">
        Thank you for using my website! 😊
        Your response has been successfully recorded <3
        You may now close the tab 🌸
        
    </div>

   

    <!-- 🌸 Copyright -->
    <div class="copyright">
        © 2025 by Camellia Banerjee
    </div>

    <!-- 🌸 JavaScript for Form Submission and Pop-Up -->
    <script>
        document.getElementById('qaForm').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent the form from submitting

            // Get form data
            const formData = new FormData(event.target);

            // Convert form data to URL-encoded string
            const urlEncodedData = new URLSearchParams(formData).toString();

            // Send data to Google Forms
            fetch('https://docs.google.com/forms/d/e/1FAIpQLSfTybyWbnYvin_S8t04Dh47xfsLvIe1jva3yZ8vV_W9p6VNnw/formResponse', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/x-www-form-urlencoded',
                },
                body: urlEncodedData,
                mode: 'no-cors', // Required for Google Forms
            })
            .then(() => {
                // Show the pop-up and overlay
                document.getElementById('popup').style.display = 'block';
                document.getElementById('overlay').style.display = 'block';

                // Hide the pop-up and overlay after 25 seconds
                setTimeout(function() {
                    document.getElementById('popup').style.display = 'none';
                    document.getElementById('overlay').style.display = 'none';
                }, 25000); // 25 seconds (25000 milliseconds)
            })
            .catch((error) => {
                console.error('Error submitting form:', error);
            });
        });
    </script>

</body>
</html>
