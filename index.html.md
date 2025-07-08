<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>Brutallost - Coming Soon</title>  
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">  
    <style>  
        body {  
            margin: 0;  
            padding: 0;  
            font-family: 'Montserrat', sans-serif;  
             /* --- ADD THESE LINES FOR BACKGROUND IMAGE --- */
background-image: url('YOUR_IMAGE_FILENAME.jpg'); /* Replace with the actual filename you uploaded */
background-size: cover; /* Ensures the image covers the entire screen */
background-position: center center; /* Centers the image */
background-repeat: no-repeat; /* Prevents the image from repeating */
background-attachment: fixed; /* Keeps the background fixed */
/* --- END BACKGROUND IMAGE LINES --- */
/* Dark background */  
            color: #ffffff; /* White text */  
            display: flex;  
            justify-content: center;  
            align-items: center;  
            min-height: 100vh;  
            overflow: hidden; /* Prevent scrollbars */  
            position: relative;  
        }  
  
        .container {  
            text-align: center;  
            z-index: 2; /* Above particles */  
            position: relative;  
            opacity: 0; /* Start hidden for animation */  
            animation: fadeIn 2s forwards;  
        }  
  
        @keyframes fadeIn {  
            to {  
                opacity: 1;  
            }  
        }  
  
        h1 {  
            font-size: 5em; /* Large heading */  
            margin-bottom: 20px;  
            letter-spacing: 5px; /* Spaced out letters */  
            text-transform: uppercase;  
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.3);  
        }  
  
        p {  
            font-size: 1.2em;  
            margin-bottom: 40px;  
            max-width: 600px;  
            margin-left: auto;  
            margin-right: auto;  
            line-height: 1.6;  
        }  
  
        .social-links a {  
            color: #ffffff;  
            font-size: 1.5em;  
            margin: 0 15px;  
            text-decoration: none;  
            transition: color 0.3s ease;  
        }  
  
        .social-links a:hover {  
            color: #ff0055; /* A vibrant accent color on hover */  
        }  
  
        /* Particle animation (CSS only for simplicity, can be replaced with JS for more control) */  
        .particle {  
            position: absolute;  
            background-color: rgba(255, 255, 255, 0.1);  
            border-radius: 50%;  
            animation: float 20s infinite ease-in-out;  
        }  
  
        @keyframes float {  
            0% { transform: translateY(0) translateX(0); opacity: 0.5; }  
            50% { transform: translateY(-50px) translateX(50px); opacity: 1; }  
            100% { transform: translateY(0) translateX(0); opacity: 0.5; }  
        }  
  
        /* Responsive adjustments */  
        @media (max-width: 768px) {  
            h1 {  
                font-size: 3em;  
            }  
            p {  
                font-size: 1em;  
                padding: 0 20px;  
            }  
        }  
    </style>  
</head>  
<body>  
    <div class="container">  
        <h1>Brutallost</h1>  
        <p>Unleashing a new era of style. Prepare for the rebellion. Our collection is dropping soon.</p>  
        <div class="social-links">  
            <a href="#" target="_blank">Facebook</a>  
            <a href="#" target="_blank">Instagram</a>  
            <a href="#" target="_blank">Twitter</a>  
        </div>  
    </div>  
  
    <script>  
        const body = document.querySelector('body');  
        const numberOfParticles = 50;  
  
        for (let i = 0; i < numberOfParticles; i++) {  
            const particle = document.createElement('div');  
            particle.classList.add('particle');  
              
            const size = Math.random() * 5 + 2; // Random size between 2px and 7px  
            particle.style.width = `${size}px`;  
            particle.style.height = `${size}px`;  
              
            particle.style.left = `${Math.random() * 100}vw`;  
            particle.style.top = `${Math.random() * 100}vh`;  
              
            // Randomize animation duration and delay for more natural movement  
            particle.style.animationDuration = `${Math.random() * 10 + 10}s`; // 10-20s  
            particle.style.animationDelay = `${Math.random() * 5}s`; // 0-5s delay  
              
            body.appendChild(particle);  
        }  
    </script>  
</body>  
</html>  
