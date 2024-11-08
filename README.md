<!DOCTYPE html>
<html lang="en">

<head>
    <title>My Portfolio</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
    <link href="https://fonts.googleapis.com/css2?family=Lobster&display=swap" rel="stylesheet">
    <link href="style.html" rel="stylesheet">
    <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lato">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Oswald">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open Sans">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

    <!-- CSS for loader and circular image -->
    <style>
        .mmain-content {
            text-align: center;
            padding: 20px;
        }
        
        .moving-bottom-header {
            position: fixed;
            bottom: 0;
            left: 0;
            width: 100%;
            background-color: rgba(0, 248, 236, 0.26);
            color: #e74c3c;
            text-align: center;
            padding: 10px 0;
            overflow: hidden;
            font-size: 1.2rem;
            font-family: 'Times New Roman', Times, serif;
            z-index: 1000;
        }
        
        .moving-bottom-header p {
            display: inline-block;
            white-space: nowrap;
            padding-left: 100%;
            animation: slide 20s linear infinite;
        }
        
        @keyframes slide {
            from {
                transform: translateX(0);
            }
            to {
                transform: translateX(-100%);
            }
        }
        
        .aesthetic-div {
            font-family: 'Raleway', sans-serif;
            background-color: #ffffff;
            border: 2px solid;
            border-radius: 15px;
            box-shadow: 0 4px 20px;
            padding: 30px;
            margin: 20px auto;
            max-width: 600px;
            transition: transform 0.3s;
        }
        
        .aesthetic-div:hover {
            transform: translateY(-5px);
            /* Lift the div slightly on hover */
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);
            /* Deepen shadow on hover */
        }
        
        h2 {
            font-weight: 700;
            /* Bold font for heading */
            color: #2c3e50;
            /* Darker color for contrast */
        }
        
        p {
            font-weight: 400;
            /* Normal weight for paragraph */
            line-height: 1.6;
            /* Improved line spacing */
            color: #000000;
            /* Slightly lighter color for text */
        }
        
        h1 {
            font-family: 'Lobster', cursive;
            font-size: 3rem;
            color: #37f055;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s;
        }
        
        h1:hover {
            transform: scale(1.1);
            /* Slightly enlarge on hover */
            color: #e74c3c;
            /* Change color on hover */
        }
        
        h2 {
            font-family: 'Lobster', cursive;
            /* Same font for a cohesive look */
            font-size: 2rem;
            color: #8e44ad;
            /* Another aesthetic color */
            margin-top: 20px;
        }
        
        .content {
            position: relative;
            z-index: 1;
            color: white;
            text-align: center;
            padding: 20px;
        }
        
        .fb-logo {
            position: absolute;
            bottom: 20px;
            left: 20px;
            width: 50px;
            height: auto;
            z-index: 1;
            /* Ensure logo is above the video */
        }
        
        .swipe {
            animation: swipe-in 0.6s forwards;
        }
        
        @keyframes swipe-in {
            0% {
                transform: translateX(-100%);
            }
            100% {
                transform: translateX(0);
            }
        }
        
        .circle-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
        }
        
        .animated-title {
            opacity: 0;
            transform: translateY(50px);
            animation: entrance 1s forwards;
        }
        
        @keyframes entrance {
            0% {
                opacity: 0;
                transform: translateY(50px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .custom-cursor {
            position: absolute;
            width: 30px;
            height: 30px;
            background-color: rgba(255, 0, 0, 0.7);
            border-radius: 50%;
            pointer-events: none;
            transform: translate(-50%, -50%);
            transition: background-color 1s;
        }
        
        body:hover .custom-cursor {
            background-color: #37f055;
        }
    </style>
</head>

<body>

    <div class="custom-cursor" id="customCursor"></div>
    <script>
        const customCursor = document.getElementById('customCursor');

        document.addEventListener('mousemove', (event) => {
            const mouseX = event.clientX;
            const mouseY = event.clientY;
            customCursor.style.left = `${mouseX}px`;
            customCursor.style.top = `${mouseY}px`;
        });
    </script>


    <!-- Ensure the logo path is correct -->
    <div class="w3-bar w3-black w3-hide-small swipe">
        <a href="https://www.facebook.com/profile.php?id=61561110523865" class="w3-bar-item w3-button"><i class="fa fa-facebook-official"></i></a>
        <a href="#" class="w3-bar-item w3-button"><i class="fa fa-instagram"></i></a>
        <a href="#" class="w3-bar-item w3-button"><i class="fa fa-snapchat"></i></a>
        <a href="#" class="w3-bar-item w3-button"><i class="fa fa-flickr"></i></a>
        <a href="#" class="w3-bar-item w3-button"><i class="fa fa-twitter"></i></a>
        <a href="#" class="w3-bar-item w3-button"><i class="fa fa-linkedin"></i></a>
        <a href="#" class="w3-bar-item w3-button w3-right"><i class="fa fa-search"></i></a>

    </div>
    <div class="w3-row">
        <div class="w3-half w3-black w3-container w3-center" style="height:800px">
            <div class="w3-padding-64">
                <h1 class="animated-title">My Logo</h1>
            </div>
            <div class="w3-padding-64 swipe">


                <a href="resume_final_web.html" class="w3-button w3-black w3-block w3-hover-dark-grey w3-padding-18">Resume</a>
                <a href="calculator.html" class="w3-button w3-black w3-block w3-hover-brown w3-padding-18">calculator</a>
                <a href="send_a_message.html" class="w3-button w3-black w3-block w3-hover-brown w3-padding-18">Send A Message</a>
                <a href="chat_box.html" class="w3-button w3-black w3-block w3-hover-brown w3-padding-18">Chat Box</a>
            </div>
        </div>
        <div class="w3-half w3-blue-grey w3-container" style="height: 800px">
            <div class="w3-padding-64 w3-center">
                <h1 class="animated-title">About Me</h1>
                <img src="main_picture.jpg" class="circle-img swipe" alt="My Picture">
                <!-- Ensure this path is correct -->
                <div class="w3-left-align w3-padding-large swipe aesthetic-div">
                    <p>Hello! I'm an aspiring IT professional with a focus on Basic Web Programming and a solid foundation as an I.T. Technician. I am currently pursuing a Bachelor of Science in Information Technology at Cebu Roosevelt Memorial Colleges,
                        where I have been honing my technical skills and deepening my knowledge in the field of technology.</p>
                    <p>I am willing to learn and continuously seek opportunities to expand my expertise. Whether it's web development, troubleshooting, or exploring new technologies, I am driven by a passion for creating efficient solutions and embracing
                        growth. I'm excited to apply my skills in real-world projects and contribute to the dynamic field of IT.</p>
                </div>
                <div class="moving-bottom-header">
                    <p> A Simple Website Made By Christian N Regala CRMC Student with a Degree Of Bachelor Of Science In Information Technology</p>

                </div>
            </div>
        </div>
    </div>
</body>

</html>
