# Text Components
Please reach out if something isn't working like you think it should - or if you want alterations. Or even if you have more ideas and want to know how to do them!

All of these components go inside the `<main class="outer-container">` element.

Add section headers!

## Common CSS Properties
Each property has more values, I just listed some common ones. Comprehensive list: https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals

`color: ` sets the font color. Values can be `red` or any other browser-preset colors, `rgb(#, #, #);` where # is a number 0 - 255, or a hex value (`#XXYYZZ`) where XX, YY, and ZZ are hexadecimal values.

`text-align: ` values can be `left`, `right`, or `center`.

`font-weight: ` value can be `bold`.

`font-family: ` values can be generic (`cursive`, `serif`, `sans-serif`, `monospace`) or family name (`Arial`, `Times New Roman`, `Verdana`, `Georgia`) 

`font-size: ` values can be `#px` where # is a number.

`font-style: ` value can be `italic`.

`text-decoration: ` values can be `none` (removes underline) and `underline`.

## Main Heading
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/144962464-ca05b635-4cf9-4518-a846-424035f3c473.png">
</p>
This can be your name, title, short description, etc.

#### HTML
```
<h1 class="title">Your Name</h1>
```
#### CSS
```
.title {
    font-size: 10vw; /*Resize as you see fit. This sets the height to 10% of the width of the window*/
    color: olivedrab; /* Change color to what you want. Remove this for black font. */
}
```
## Small Blurb
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/145343054-34060fea-d877-4989-a4cd-30ee42b20b35.png">
</p>

#### HTML
```
<p class="small-blurb">I am an innovator.</p>
```

#### CSS
```
.small-blurb {
    font-variant: small-caps;
}
```

##### @media only screen and (max-width: 600px)
```
.small-blurb {
    font-size: 1.5em;
}
```
##### @media only screen and (min-width: 601px)
```
.small-blurb {
    font-size: 2.3em;
}
```
##### @media only screen and (min-width: 1000px)
```
.small-blurb {
    font-size: 3em;
}
 ```
## Long Blurb
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/145344111-b57c9b52-59bd-4aed-b331-d2508e187d74.png">
</p>

#### HTML
```
<p class="long-blurb">
    Hey, here is where you can add a longer blurb about yourself.
    Add as much information as you like. Ideas: how you got to where you are now, 
    what you do now, what you'd like to do.<br><br>Add a line break with the &lt;br&gt; 
    element to make another paragraph in the longer blurb.
</p>
```
## Section Title
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/145599973-97fe015c-ade5-4188-81a6-3ea1a32039d2.png">
</p>

Each section title element should have an `id` attribute whose value is the section name (with no spaces - instead dashes or capitalization)

Ex) \[Skills Summary] -> `skills-summary` or `skillsSummary`]

This is used for navigation in the nav bar.

#### HTML
```
<h2 class="section-title" id="biography">
    Biography
</h2>
```
#### CSS
```
.section-title {   
    color: darkcyan;
    width: 100%;
    padding-bottom: 5px;
    border-bottom: darkcyan 2px solid;
}
```
## Section Content
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/145626762-c1c89960-8971-492b-ba9a-6ac04463ae4f.png">
</p>

#### HTML
```
<div class="section-content">
    <div class="sc-heading">
        <span class="position">Innovator</span>
        <span class="time">May 2009 - June 2012</span>
    </div>
    <p class="sc-location">Solutions Co.</p>
    <p class="sc-description">
        As an innovator, I completed X, Y, and Z.
        <a class="sc-link" href="#">Check out the changes here!</a>
        <!-- Replace the '#' in href to a URL link -->
    </p>
    <div class="sc-skills-container">
        <span class="sc-skill">MS Word</span>
        <span class="sc-skill">Python</span>
        <span class="sc-skill">Excel</span>
        <span class="sc-skill">Rest APIs</span>
        <span class="sc-skill">AWS</span>
    </div>
    <ul class="sc-list">
        <li class="sc-item">Created a solution for X which lowered processing time from Yms to Zms</li>
        <li class="sc-item">Responsibility 2</li>
    </ul>
</div>
```
#### CSS 
```
.sc-skills-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
.section-content {
    width: 100%;
    margin-top: 10px;
}
.sc-heading {
    width: 100%;
    display: flex;
    align-items: center;
}
.position {
    max-width: 300px;
    word-wrap: break-word;
    font-size: 1.4em;
}
.time {
    padding-left: 10px;
    margin-left: auto;
    font-style: italic;
}
.sc-link {
    text-decoration: none;
    color: slateblue;
}
.sc-link:hover {
    text-decoration: none;
    color: darkslateblue;
}
.sc-description {
    margin-bottom: 5px;
}
.sc-skill {
    border: 1px solid darkcyan;
    color: darkcyan;
    margin: 5px 10px;
    border-radius: 5px;
    padding: 2px 4px; 
    font-size: .9em;
}
.sc-location {
    margin: 0px;
}
```
##### @media only screen and (max-width: 600px)
```
.sc-heading {
    width: 100%;
    display: block;
    align-items: center;
}
.position {
    width: 100%;
    word-wrap: break-word;
    font-size: 1.4em;
    display: block;
}
.time {
    padding: 0px;
    width: 100%;
    font-style: italic;
}
```
## Item Grid List
<p align="center">
  <img height="300px" src="https://user-images.githubusercontent.com/43857043/145654571-99b66226-e25e-4e60-8c44-496810b0ff0f.png">
</p>

Can display skills, achievements, awards, etc. The `item-level` and `item-desc` elements can be considered optional.

#### HTML
I removed a couple of the `li` elements in this HTML so not all items in the image are listed below.
```
<ul class="items-grid">
    <li class="item">
        <p class="item-name">HTML & CSS</p>
        <p class="item-level">Knowledgable</p>
        <p class="item-desc">Created several sample websites using HTML & CSS</p>
    </li>
    <li class="item">
        <p class="item-name">TOPS Award</p>
        <p class="item-desc">Awarded greatest contributer to development of Pre-K learning program</p>
    </li>
</ul>
```

#### CSS
```
.items-grid {
    display: flex;
    flex-wrap: wrap;
    padding: 0px;
    justify-content: space-between;
}
.item {
    list-style-type: none;
    padding: 10px 0px;
    display: list-item;
    box-sizing: border-box;
}
.item-name {
    font-size: 1.4em;
    margin: 0px;
    font-weight: bold;
    color: teal;
    text-shadow: -1px 1px #c2c2c2;
}
.item-level {
    margin: 0px;
    font-variant: small-caps;
}
```

##### @media only screen and (max-width: 600px)
```
.item {
    width: 100%;
}
```

##### @media only screen and (min-width: 601px)
```
.item {
    width: 48%;
}
```

## Contact Me Section
<p align="center">
  <img height="300px" src="https://user-images.githubusercontent.com/43857043/145663124-3368e64d-a8c4-4143-b984-7339d7840b07.png">
</p>

This component uses the code found at /main-blocks/buttons-and-links/ Social Media Icons section. Please refer to [here](https://github.com/MorganHaworth/Sample-Portfolio-Components/tree/main/main-blocks/buttons-and-links#social-media-icons-square-and-circle).

Include as much information as you are comfortable sharing online.

#### HTML
```
<div class="contact-section">
    <p class="contact">Firstname Lastname in Omaha, NE</p>
    <div class="email-section">
        <p class="contact">Email</p>
        <a target="_blank" href="mailto:youremail@mail.com">Email Me</a>
    </div>
    <p class="contact">Phone</p>
    <p class="contact-info">+1 (XXX) XXX - XXXX</p>
    <p class="contact">On the Web</p>
    <div class="icon-container">
        <a href="#your-link" class="fa icon fa-linkedin"></a>
        <a href="#your-link" class="fa icon fa-envelope"></a>
    </div>
</div>
```

#### CSS
```
.contact-section {
    text-align: left;
    width: 100%;
    margin: 0px;
}
.contact {
    margin-bottom: 5px;
    font-size: 1.2em;
}
.contact-info {
    margin: 5px 20px 20px;
}
.email-section a {
    display: block;
    background: rgb(226, 226, 226); /* Color of button: Change this to a color you like */
    padding: 20px 30px;
    border-radius: 15px;
    border: none;
    box-shadow: 0px 4px 5px 0px lightgray;
    margin: auto;
    box-sizing: border-box;
    font-weight: bold;
    text-align: center;
    font-size: 1.2em;
    text-decoration: none;
    color: rgb(50,50,50); /* Font color: Change this to a color you like */
}
.email-section a:hover {
    box-shadow: 0px 4px 5px 0px darkgray;
}
```
##### @media only screen and (max-width: 600px)
```
.email-section a {
    width: 100%;
}
```
