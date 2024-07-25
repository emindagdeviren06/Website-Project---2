# Website-Project---2
Created a basic website using HTML, CSS, and JavaScript





First Page Preview:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Welcome to HotBeansWeb's Website">
    <meta name="keywords" content="HotBeansWeb, website, welcome">
    <title>Home</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: sans-serif;
            color: #fff;
            background-image: url('background.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            min-height: 100vh;
        }

        header {
            background: rgba(0, 0, 0, 0.5);
            padding: 1em 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            top: 0; /* Position header at the top */
            width: 100%;
            z-index: 1;
        }

        .page-title {
            margin-left: 20px;
            font-size: 24px;
            font-weight: 700;
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin-right: 20px;
        }

        nav ul li {
            display: inline;
            margin: 0 10px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
        }

        .home-section {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding-top: 100px;
            margin-top: 60px; /* Adjusted margin to avoid overlap with header */
        }

        .video-container {
            width: 80%; /* Adjusted width for mobile */
            max-width: 700px;
            border: 3px solid #fff;
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 20px;
        }

        video {
            width: 100%;
            height: auto;
        }

        .welcome-text {
            font-family: 'Times New Roman', serif;
            font-size: 36px; /* Adjusted font size for mobile */
            color: #000;
            margin-top: 10px;
            font-weight: bold;
        }

        footer {
            background: rgba(0, 0, 0, 0.5);
            color: #fff;
            text-align: center;
            padding: 1em 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        .accessibility-button {
            position: fixed;
            bottom: 70px;
            right: 20px;
            background-color: #000;
            color: #fff;
            border: none;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            font-size: 24px;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 2;
        }

        .accessibility-panel {
            display: none;
            position: fixed;
            bottom: 130px;
            right: 20px;
            background-color: rgba(0, 0, 0, 0.8);
            color: #fff;
            padding: 20px;
            border-radius: 10px;
            z-index: 2;
        }

        .accessibility-panel button {
            background-color: #fff;
            color: #000;
            border: none;
            margin: 5px;
            padding: 10px;
            cursor: pointer;
        }

        @media screen and (max-width: 768px) {
            .video-container {
                width: 90%; /* Adjusted width for smaller screens */
            }

            .welcome-text {
                font-size: 24px; /* Adjusted font size for smaller screens */
            }
        }
    </style>
    <script>
        function toggleAccessibilityPanel() {
            var panel = document.getElementById('accessibility-panel');
            if (panel.style.display === 'none' || panel.style.display === '') {
                panel.style.display = 'block';
            } else {
                panel.style.display = 'none';
            }
        }

        function increaseFontSize() {
            document.body.style.fontSize = 'larger';
        }

        function decreaseFontSize() {
            document.body.style.fontSize = 'smaller';
        }
    </script>
</head>
<body>
    <header>
        <h1 class="page-title">Home</h1>
        <nav>
            <ul>
                <li>
                    <li><a href="apply.html">Apply</a></li>
                    <li><a href="about.html">About Us</a></li>
                    <li><a href="team.html">Our Team</a></li>
                    <li><a href="courses.html">Courses</a></li>
                    <li><a href="contact.html">Contact Us</a></li>
                    <li><a href="boy.html">Boy</a></li> <!-- New link -->
                </ul>
            </nav>
        </header>
        <section class="home-section">
            <div class="video-container">
                <video controls>
                    <source src="video.mp4" type="video/mp4">
                    Your browser does not support the video tag.
                </video>
            </div>
            <div class="welcome-text">Welcome to our website</div>
        </section>
        <footer>
            <p>&copy; 2024 Our Company</p>
        </footer>
        <button class="accessibility-button" onclick="toggleAccessibilityPanel()">A</button>
        <div class="accessibility-panel" id="accessibility-panel">
            <button onclick="increaseFontSize()">Increase Font Size</button>
            <button onclick="decreaseFontSize()">Decrease Font Size</button>
            <button onclick="toggleContrast()">Toggle High Contrast</button>
        </div>
        <script>
            function toggleContrast() {
                document.body.classList.toggle('high-contrast');
            }
        </script>
    </body>
    </html>
