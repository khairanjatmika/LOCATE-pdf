<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LOCATE : VISUAL BRANDING PRESENTATION</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
            background-color: #f4f4f4;
        }
        .container {
            max-width: 100%;
            margin: auto;
            padding: 20px;
        }
        .image-container {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .image-container img {
            width: 100%;
            max-width: 800px;
            margin-bottom: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .nav-buttons {
            margin-top: 20px;
        }
        .nav-buttons button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            margin: 5px;
            border: none;
            border-radius: 5px;
            background-color: #007BFF;
            color: white;
        }
        .nav-buttons button:disabled {
            background-color: #ccc;
            cursor: not-allowed;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>LOCATE : VISUAL BRANDING PRESENTATION</h1>
        <div class="image-container">
            <img id="slide" src="slide 1.png" alt="Slide 1">
        </div>
        <div class="nav-buttons">
            <button id="prev" onclick="prevSlide()" disabled>Previous</button>
            <button id="next" onclick="nextSlide()">Next</button>
        </div>
    </div>

    <script>
        const slides = [
            "slide 1.png", "slide 2.png", "slide 3.png", "slide 4.png", "slide 5.png",
            "slide 6.png", "slide 7.png", "slide 8.png", "slide 9.png", "slide 10.png",
            "slide 11.png", "slide 12.png", "slide 13.png", "slide 14.png", "slide 15.png"
        ];
        let currentIndex = 0;

        function updateSlide() {
            document.getElementById("slide").src = slides[currentIndex];
            document.getElementById("prev").disabled = currentIndex === 0;
            document.getElementById("next").disabled = currentIndex === slides.length - 1;
        }

        function nextSlide() {
            if (currentIndex < slides.length - 1) {
                currentIndex++;
                updateSlide();
            }
        }

        function prevSlide() {
            if (currentIndex > 0) {
                currentIndex--;
                updateSlide();
            }
        }
    </script>
</body>
</html>
