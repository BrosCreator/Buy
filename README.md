<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Buy</title>
    <style>
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
            <button onclick="showSlide(1)">Product 1</button>
            <button onclick="showSlide(2)">Product 2</button>
            <button onclick="showSlide(3)">Product 3</button>
        </nav>
    </header>

 <main>
        <section class="slide active-slide" id="slide1">
            <h2>Product 1</h2>
            <p>This is the content of Product 1.</p>
        </section>
        <section class="slide" id="slide2">
            <h2>Product 2</h2>
            <p>This is the content of Product 2.</p>
        </section>
        <section class="slide" id="slide3">
            <h2>Product 3</h2>
            <p>This is the content of Product 3.</p>
        </section>
    </main>

 <footer>
        <p>&copy; 2024 Your Website</p>
    </footer>

 <script>
        function showSlide(slideNumber) {
            var slides = document.querySelectorAll('.slide');
            slides.forEach(function(slide) {
                slide.classList.remove('active-slide');
            });
            document.getElementById('slide' + slideNumber).classList.add('active-slide');
        }
    </script>
</body>
</html>
