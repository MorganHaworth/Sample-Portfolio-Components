# Text Components
Please reach out if something isn't working like you think it should - or if you want alterations. Or even if you have more ideas and want to know how to do them!

All of these components go inside the `<div class="outer-container">` element.

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
##### @media only screen and (min-width: 600px)
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

#### HTML
```
<h2 class="section-title">
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
## Section Content 1
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/145626762-c1c89960-8971-492b-ba9a-6ac04463ae4f.png">
</p>

#### HTML
```
<div class="section-content-1">
    <div class="sc1-heading">
        <span class="position-1">Innovator</span>
        <span class="time-1">May 2009 - June 2012</span>
    </div>
    <p class="sc1-location">Solutions Co.</p>
    <p class="sc1-description">
        As an innovator, I completed X, Y, and Z.
        <a class="sc1-link" href="#">Check out the changes here!</a>
        <!-- Replace the '#' in href to a URL link -->
    </p>
    <div class="sc1-skills-container">
        <span class="sc1-skill">MS Word</span>
        <span class="sc1-skill">Python</span>
        <span class="sc1-skill">Excel</span>
        <span class="sc1-skill">Rest APIs</span>
        <span class="sc1-skill">AWS</span>
    </div>
    <ul class="sc1-list">
        <li class="sc1-item">Created a solution for X which lowered processing time from Yms to Zms</li>
        <li class="sc1-item">Responsibility 2</li>
    </ul>
</div>
```
#### CSS 
```
.section-title {   
    color: darkcyan;
    width: 100%;
    padding-bottom: 5px;
    border-bottom: darkcyan 2px solid;
}
.sc1-skills-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
.section-content-1 {
    width: 100%;
    margin-top: 10px;
}
.sc1-heading {
    width: 100%;
    display: flex;
    align-items: center;
}
.position-1 {
    max-width: 300px;
    word-wrap: break-word;
    font-size: 1.4em;
}
.time-1 {
    padding-left: 10px;
    margin-left: auto;
    font-style: italic;
}
.sc1-link {
    text-decoration: none;
    color: slateblue;
}
.sc1-link:hover {
    text-decoration: none;
    color: darkslateblue;
}
.sc1-description {
    margin-bottom: 5px;
}
.sc1-skill {
    border: 1px solid darkcyan;
    color: darkcyan;
    margin: 5px 10px;
    border-radius: 5px;
    padding: 2px 4px; 
    font-size: .9em;
}
.sc1-location {
    margin: 0px;
}
```
##### @media only screen and (max-width: 600px)
```
.sc1-heading {
    width: 100%;
    display: block;
    align-items: center;
}
.position-1 {
    width: 100%;
    word-wrap: break-word;
    font-size: 1.4em;
    display: block;
}
.time-1 {
    padding: 0px;
    width: 100%;
    font-style: italic;
}
```
