<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Title Here</title>
    <style>
        /* Add your CSS styles here */
        .slide {
            display: none;
        }

        .active-slide {
            display: block;
        }
    </style>
</head>
<body>
    <header>
        <h1>Your Website Title</h1>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="slide active-slide" id="slide1">
            <h2>Section 1</h2>
            <p>This is the content of section 1.</p>
        </section>
        <section class="slide" id="slide2">
            <h2>Section 2</h2>
            <p>This is the content of section 2.</p>
        </section>
        <section class="slide" id="slide3">
            <h2>Section 3</h2>
            <p>This is the content of section 3.</p>
        </section>

        <!-- Button to show next slide -->
        <button id="showSlideBtn">Show Next Slide</button>

        <script>
            var currentSlideIndex = 1;
            var totalSlides = 3;

            document.getElementById("showSlideBtn").addEventListener("click", function() {
                var currentSlide = document.getElementById("slide" + currentSlideIndex);
                currentSlide.classList.remove("active-slide");
                currentSlideIndex = (currentSlideIndex % totalSlides) + 1;
                var nextSlide = document.getElementById("slide" + currentSlideIndex);
                nextSlide.classList.add("active-slide");
            });
        </script>
    </main>

    <footer>
        <p>&copy; 2024 Your Website</p>
    </footer>
</body>
</html>
