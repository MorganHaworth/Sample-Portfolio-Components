# Images

Please reach out if something isn't working like you think it should - or if you want alterations. Or even if you have more ideas and want to know how to do them!

## Circular Image
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/144562096-4acc069c-2ab7-480d-b6d4-930de17428bb.png">
</p>

Can be used as a primary photo of yourself, personal brand icon, or any photo. You will need to place an image `blank-profile-picture.png` in the `assets/` folder at root.

Goes inside the `<div class="outer-container">` element.
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

Goes inside the `<div class="outer-container">` element.
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

Be mindful of how much text you include in this component. If you want to swap side, swap the left and right values for the float property per media query. You will need to place an image `landscape.jpg` in the `assets/` folder at root.

Goes inside the `<div class="outer-container">` element.
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
##### @media only screen and (min-width: 600px)
```
.image-by-text {
    width: 50%;
    float: right;
}
.text-by-image {
    margin: 0px 2.5%;
    float: left;
    width: 45%;
}
```
##### @media only screen and (min-width: 1000px)
```
.image-by-text {
    width: 50%;
    float: right;
}

.text-by-image {
    margin: 0px 5%;
    float: left;
    width: 40%;
    font-size: 1.15em;
}
```
