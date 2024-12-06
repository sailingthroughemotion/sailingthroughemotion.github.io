---
layout: default
---

# FALL 2024 SEMESTER PROJECT: Visual System Design

I have to admit that this is placeholder text on a static web-page that is not available from the main index of my website. The website in general needs to be re-arranged to accomodate my student work again, as currently it's focused entirely on professional/commissioned work. A write-up explaining this project and why it had been made would go here.

<div class="carousel">
  <div class="carousel-images">
    <img src="https://i.imgur.com/vFWmgHq.png">
    <img src="https://i.imgur.com/5kVkVeM.png">
    <img src="https://i.imgur.com/C3J0Vhi.png">
    <img src="https://i.imgur.com/npSD8jm.png">
    <img src="https://i.imgur.com/kKzyiCE.png">
    <img src="https://i.imgur.com/Stj4X6U.png">
    <img src="https://i.imgur.com/zf8C4cu.png">
    <img src="https://i.imgur.com/jqcwuYO.png">
    <img src="https://i.imgur.com/vCLf6Gq.png">
    <img src="https://i.imgur.com/HibbMU1.png">
  </div>
  <button class="prev" onclick="moveSlide(-1)">&#10094;</button>
  <button class="next" onclick="moveSlide(1)">&#10095;</button>
</div>

<script>
  let index = 0;

  function moveSlide(direction) {
    const images = document.querySelectorAll('.carousel-images img');
    const totalImages = images.length;
    index = (index + direction + totalImages) % totalImages;  // Ensures looping

    const offset = -index * 100;  // Shift the carousel images
    document.querySelector('.carousel-images').style.transform = `translateX(${offset}%)`;
  }
</script>

<style>
  /* Carousel container */
.carousel {
    width: 100%;
    max-width: 600px; /* Set the maximum width of the carousel */
    margin: 0 auto; /* Center the carousel horizontally */
    position: relative;
    overflow: hidden;
}

/* Image wrapper for carousel */
.carousel-images {
    display: flex;
    transition: transform 0.5s ease-in-out;
    align-items: center; /* Vertically center images within the container */
}

/* Individual images */
.carousel-images img {
    width: 100%;
    height: auto;
    object-fit: contain;
    flex-shrink: 0; /* Prevents images from shrinking */
    display: block; /* Ensures no space below the images */
    /* Ensures the image covers the entire container without stretching */
}

/* Previous and Next buttons */
.prev, .next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    font-size: 2rem;
    padding: 10px;
    cursor: pointer;
}

.prev {
    left: 10px;
}

.next {
    right: 10px;
}

</style>


