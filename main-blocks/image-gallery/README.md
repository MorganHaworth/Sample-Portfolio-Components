# Image Gallery

Please reach out if something isn't working like you think it should - or if you want alterations. Or even if you have more ideas and want to know how to do them!

This component goes inside the `<main class="outer-container">` element.

## Image Carousel
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/145667355-521a3355-2aa6-41c2-acf3-df99f2147bca.png">
</p>

#### HTML
This contains an empty carousel and empty carousel dots. It is populated by our Javascript.
```
<div id="carousel">
    <!-- &#10094; is the < symbol -->
    <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
    <!-- &#10095; is the > symbol -->
    <a class="next" onclick="plusSlides(1)">&#10095;</a>
</div>
<div id="carousel-dots">
</div>
```

#### CSS
This CSS uses CSS animations to provide a fade between images.
```
#carousel {
    width: 100%;
    position: relative;
    margin: 25px auto;
    background-color: rgb(50,50,50);
    overflow: hidden;
}
.carousel-image-container {
    display: none;
}
.carousel-count {
    position: absolute;
    width: 100%;
    left: 10px;
    top: 0px;
    color: white;
}   
.carousel-image {
    margin: auto;
    display: block;
}
.carousel-caption {
    color: #f2f2f2;
    font-size: 15px;
    padding: 8px 12px;
    position: absolute;
    bottom: 0px;
    width: 100%;
    text-align: center;
    box-sizing: border-box;
}
.prev, .next {
    cursor: pointer;
    position: absolute;
    top: 50%;
    width: auto;
    padding: 16px;
    margin-top: -22px;
    color: white;
    font-weight: bold;
    font-size: 18px;
    transition: 0.6s ease;
    border-radius: 0 3px 3px 0;
    user-select: none;
}
.next {
    right: 0;
    border-radius: 3px 0 0 3px;
}
.prev:hover, .next:hover {
    background-color: rgba(0,0,0,.8);
}
.dot {
    cursor: pointer;
    height: 15px;
    width: 15px;
    margin: 0 2px;
    background-color: #bbb;
    border-radius: 50%;
    display: inline-block;
    transition: background-color 0.6s ease;
}

.activedot, .dot:hover {
    background-color: #717171;
}
.fade {
    -webkit-animation-name: fade;
    -webkit-animation-duration: .5s;
    animation-name: fade;
    animation-duration: .5s;
    }

    @-webkit-keyframes fade {
    from {opacity: .4} 
    to {opacity: 1}
    }

    @keyframes fade {
    from {opacity: .4} 
    to {opacity: 1}
}
```
##### @media only screen and (max-width: 600px)
This value may be adjusted to better suit your images' dimensions.
```
.carousel-image {
    height: 200px;
}
```
##### @media only screen and (min-width: 601px)
This value may be adjusted to better suit your images' dimensions.
```
.carousel-image {
    height: 400px;
}
```
### JS
The `images` variable contains a list of object. Each object has a image src path, alt description, and caption.
```
// when the page loads, it performs this function
window.onload = function() {
    // create a list of objects to hold each image's src, alt, and caption.
    let images = [
        {
            src: "assets/carousel/blue-metallic-swirls.jpg",
            alt: "blue metallic swirls",
            caption: "My blue metallic art"
        },
        {
            src: "assets/carousel/dog.jpg",
            alt: "brown puppy",
            caption: "My new puppy!"
        },
        {
            src: "assets/carousel/landscape.jpg",
            alt: "beautiful landscape",
            caption: "My last visit to the moutains"
        }, 
        {
            src: "assets/carousel/tree.png",
            alt: "tree",
            caption: "Tree"
        }
    ];

    let imageLength = images.length;
    let carousel = document.getElementById("carousel");
    let dots = document.getElementById("carousel-dots");
    
    // For each item in our imageList, we'll do the following code block
    for (let i = 0; i < imageLength; i++) {
        //create an image container
        let newImageContainer = document.createElement("div");
        newImageContainer.setAttribute("class", "carousel-image-container fade");
        
        // create an element to store the number of the image (like 1 / 3)
        let carouselCount = document.createElement("p");
        carouselCount.setAttribute("class", "carousel-count");
        carouselCount.innerHTML = i + 1 + " / " + imageLength;
        console.log("Carousel count");
        console.log(carouselCount);
  
        // add the img element and set its src and alt attributes
        let carouselImage = document.createElement("img");
        carouselImage.setAttribute("class", "carousel-image");
        carouselImage.src = images[i].src;
        carouselImage.alt = images[i].alt;
      
        //create the p element to hold the caption
        let carouselCaption = document.createElement("p");
        carouselCaption.setAttribute("class", "carousel-caption");
        carouselCaption.innerHTML = images[i].caption;
        
        //add these elements to our image container
        newImageContainer.appendChild(carouselCount);
        newImageContainer.appendChild(carouselImage);
        newImageContainer.appendChild(carouselCaption);

        //add the new image container to our carousel
        carousel.appendChild(newImageContainer);
        
        // creates a dot for each image we add
        let dot = document.createElement("span");
        dot.setAttribute("class", "dot");
        dot.setAttribute("onclick", "currentSlide(" + (i + 1) + ")");
        
        //adds the dot to our dots element
        dots.appendChild(dot);
    }
    //shows the carousel slides
    showSlides(imageIndex);
    
    //Every 10 seconds, advance to the next slide
    setInterval(function(){
        plusSlides(1)
    },10000);
}
var imageIndex = 1;
function plusSlides(n) {
    showSlides(imageIndex += n);
}

function currentSlide(n) {
    showSlides(imageIndex = n);
}

function showSlides(n) {
    let i;
    let carouselImages = document.getElementsByClassName("carousel-image-container");
    let dots = document.getElementsByClassName("dot");
    if (n > carouselImages.length) {imageIndex = 1;}
    if (n < 1) {imageIndex  = carouselImages.length;}
  
    // mades all images have no display
    for (i = 0; i < carouselImages.length; i++) {
        carouselImages[i].style.display = "none";
    }
    // makes all dots inactive
    for (i = 0; i < dots.length; i++) {
        dots[i].className = dots[i].className.replace(" activedot", "");
    }
    
    //turns the current dot active
    dots[imageIndex - 1].className += " activedot";
    //turns the current image visible
    carouselImages[imageIndex - 1].style.display = "block";
}
```
