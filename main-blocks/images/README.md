# Images

Please reach out if something isn't working like you think it should - or if you want alterations. Or even if you have more ideas and want to know how to do them!

All of these components go inside the `<main class="outer-container">` element.

## Circular Image
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/144562096-4acc069c-2ab7-480d-b6d4-930de17428bb.png">
</p>

Can be used as a primary photo of yourself, personal brand icon, or any photo. You will need to place an image `blank-profile-picture.png` in the `assets/` folder at root.

#### HTML
```
<img class="circle-image"
  src="assets/blank-profile-picture.png"
  alt="Description of image">
```
#### CSS
```
.circle-image {
    margin: 40px 0px;
    border-radius: 50%;
    max-width: 50%;
}
```
## Full Width Image
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/144563908-a50f5bbd-7ba8-4c11-bde6-fabfdc29e8c8.png">
</p>

This image should be wide and not tall. If it's tall, then it will be a lot of scrolling to view the full image. You will need to place an image `landscape.jpg` in the `assets/` folder at root.

#### HTML
```
<img class="full-image" 
  src="assets/landscape.jpg"
  alt="Replace this with a description of your image">
```
#### CSS
```
.full-image {
    display: block;
    width: 100%;
    margin: 40px 0px;
}
```

## Image and Text
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/144568357-1e067648-7b77-43e3-af7d-f3580891e2bc.png">
</p>

Be mindful of how much text you include in this component. If you want to swap side, swap the left and right values for the float property per media query. You will need to place an image `sample.jpg` in the `assets/` folder at root.

#### HTML
```
<img class="image-by-text" 
    src="assets/sample.jpg"
    alt="blue metalic swirl art">
<p class="text-by-image">
    Put text here
</p>
```
#### CSS
##### @media only screen and (max-width: 600px)
```
.image-by-text {
    width: 100%;
}
```
##### @media only screen and (min-width: 601px)
```
.image-by-text {
    width: 50%;
    float: right;
    margin: 10px;
}
.text-by-image {
    margin: 0px 2.5%;
    float: left;
    width: 45%;
}
```
##### @media only screen and (min-width: 1000px)
```
.text-by-image {
    margin: 0px 5%;
    float: left;
    width: 40%;
}
```
## Image Gallery
<p align="center">
  <img height="250px" src="https://user-images.githubusercontent.com/43857043/144959255-4033410d-09c7-4843-ac6d-860010ce08eb.png">
</p>
White space between images optional (how-to in CSS section) - Please ask questions if you need help!

#### HTML
```
<div class="image-gallery">
  <!-- Add more images to the gallery by adding more <img> elements -->
  <img src="assets/blue-metallic-swirls.jpg"
    alt="blue metalic swirl art">
</div>
```
#### CSS
```
.image-gallery {
    line-height: 0;
    -webkit-column-gap: 30px;
    -moz-column-gap: 30px;
    column-gap: 0px; /*WHITE SPACE ALTERATION-->  CHANGE column-gap: 0px; TO column-gap: 10px;*/
    margin: 30px 0px;
}
.image-gallery img {
    width: 100% !important;
    height: auto !important;
    /*WHITE SPACE ADDITION-->  margin: 5px 0px;*/
}
```
##### @media only screen and (max-width: 600px)
```
.image-gallery {
    -moz-column-count: 1;
    -webkit-column-count: 1;
    column-count: 1;
}
```
##### @media only screen and (min-width: 601px)
```
.image-gallery {
    -moz-column-count: 2;
    -webkit-column-count: 2;
    column-count: 2;
}
```
##### @media only screen and (min-width: 1000px)
```
.image-gallery {
    -moz-column-count: 3;
    -webkit-column-count: 3;
    column-count: 3;
}
 ```
 ## Background Static Image
<p align="center">
  <img height="250px" src="https://user-images.githubusercontent.com/43857043/145321725-6fc37817-f7d2-4dc7-97a1-a236d4b95eab.png">
</p>
This gives provides a background image that stays stationary in the background as you scroll. The main content is given a solid or slightly transparent background to contrast it against the background image.

#### CSS
Modify existing `body` and `.outer-container` style rules to have the additional declarations. Replace `assets/swirl-art2.jpg` with an image of your choice. The larger the image the better because otherwise it may be blurry.
```
body {
    background-image: url('assets/swirl-art2.jpg');
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-size: 100% 100%;
}
.outer-container {
  background-color: rgba(255,255,255,.9); /*This 4th value is 90% opacity. Remove the 4th value entirely for a solid color.*/
  padding: 0px 50px;
}
```
