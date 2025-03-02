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

        /* 🌸 Decorative Images */
        .strawberry {
            position: absolute;
            top: 10px;
            left: 10px;
            width: 200px; /* Increased size */
            background: transparent !important; /* Ensure no background */
        }
        
        .duck {
            position: fixed;
            bottom: 10px;
            right: 10px;
            width: 150px; /* Increased size */
            background: transparent !important; /* Ensure no background */
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

        /* 🌸 Media Queries for Responsiveness */
        @media (max-width: 768px) {
            /* Adjust for iPad and smaller screens */
            .container {
                padding: 20px;
            }
            .strawberry {
                width: 150px; /* Adjusted size for smaller screens */
            }
            .duck {
                width: 120px; /* Adjusted size for smaller screens */
            }
        }

        @media (max-width: 480px) {
            /* Adjust for mobile phones */
            body {
                padding: 10px;
            }
            .container {
                padding: 15px;
            }
            h1 {
                font-size: 18px;
            }
            input {
                width: 100%;
            }
            .strawberry {
                width: 120px; /* Adjusted size for mobile */
            }
            .duck {
                width: 100px; /* Adjusted size for mobile */
            }
        }
    </style>
</head>
<body>

    <!-- 🌸 Decorative Images -->
    <img src="https://i.imgur.com/your-transparent-strawberry.png" alt="Strawberry" class="strawberry">
    <img src="https://i.imgur.com/your-transparent-duck.png" alt="Duck" class="duck">

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
    </div>

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

                // Hide the pop-up and overlay after 10 seconds
                setTimeout(function() {
                    document.getElementById('popup').style.display = 'none';
                    document.getElementById('overlay').style.display = 'none';
                }, 10000); // 10 seconds (10000 milliseconds)
            })
            .catch((error) => {
                console.error('Error submitting form:', error);
            });
        });
    </script>

</body>
</html>


       

 
