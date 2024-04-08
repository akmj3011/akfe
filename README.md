<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>이미지 슬라이드 쇼</title>
<style>
    .slideshow-container {
        position: relative;
        max-width: 1000px;
        margin: auto;
    }

    .slides {
        display: none;
    }

    .slide-img {
        width: 100%;
        height: auto;
    }

    .prev, .next {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        font-size: 18px;
        cursor: pointer;
        padding: 16px;
        background-color: rgba(0, 0, 0, 0.5);
        color: white;
    }

    .prev {
        left: 0;
    }

    .next {
        right: 0;
    }
</style>
</head>
<body>

<div class="slideshow-container">
    <div class="slides">
        <img class="slide-img" src="cat.jpg" alt="고양이">
        <img class="slide-img" src="dog.jpg" alt="강아지">
        <img class="slide-img" src="raccoon.jpg" alt="너구리">
        <img class="slide-img" src="rabbit.jpg" alt="토끼">
    </div>
    <a class="prev" onclick="plusSlides(-1)">❮</a>
    <a class="next" onclick="plusSlides(1)">❯</a>
</div>

<script>
    var slideIndex = 1;
    showSlides(slideIndex);

    function plusSlides(n) {
        showSlides(slideIndex += n);
    }

    function showSlides(n) {
        var i;
        var slides = document.getElementsByClassName("slides");
        if (n > slides.length) {slideIndex = 1}
        if (n < 1) {slideIndex = slides.length}
        for (i = 0; i < slides.length; i++) {
            slides[i].style.display = "none";
        }
        slides[slideIndex-1].style.display = "block";
    }
</script>

</body>
</html>
