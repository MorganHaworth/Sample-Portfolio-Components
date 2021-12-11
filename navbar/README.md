# Responsive Navbar

Place this as the first element of your  `<body>` element in the HTML. This goes **outside and above** the `<main class="outer-container">` element.
This navbar is used to automatically scroll to the section headers in your portfolio. The links in the navbar point to the `id`s of your section headers.

Derived from W3 schools: https://www.w3schools.com/howto/tryit.asp?filename=tryhow_js_topnav

<p align="center">
  <img height="65px" src="https://user-images.githubusercontent.com/43857043/145660638-750fd326-8dee-4506-9e6d-5c5378166bf7.png">
</p>

If not already present, add this `<link>` element inside the `<head></head>`.
```
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
```
You may have to adjust padding and font sizes depending on then number of links you have in your navbar.

## Original

#### HTML
```
<nav id="nav">
    <ul>
        <!-- The onclick event will activate our javascript function -->
        <li><a class="hamburger-button" onclick="activateBurger()">
            <i class="hamburger fa fa-bars"></i>
        </a></li>
        <li><a href="#">Home</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#awards">Awards</a></li>
    </ul>
</nav>
```
#### CSS
```
nav {
    top: 0;
    background: teal;
    box-shadow: 0 0 6px 0 rgb(0, 0, 0, .6);
    position: sticky;
    width: 100%;
}
nav ul { /* selects ul element in nav element */
    margin: 0px;
    padding: 0px;
}
nav ul li {
    list-style-type: none;
}
nav ul li a {
    padding: 0px 18px;
    box-sizing: border-box;
}
nav ul li:hover {
    background-color: darkslategray;
}
nav a { /* selects a in nav */
    line-height: 56px;
    text-align: center;
    color: white;
    text-decoration: none;
}
```

##### @media only screen and (max-width: 600px)
```
nav a, nav li:not(:first-child) { /*selects a and li (not li containing hamburger)*/
    display: none;
}
nav li .hamburger-button { /* selects hamburger-button in li in nav when responsive is enabled */
    display: block;
    cursor: pointer;
}
nav.responsive a { /* selects a in nav when responsive is enabled */
    display: block;
}
nav.responsive ul { /* selects ul in nav when responsive is enabled */
    position: relative;
}
nav.responsive li { /* selects li in nav when responsive is enabled */
    float: none;
    display: block;
    text-align: left;
}
```

##### @media only screen and (min-width: 601px)
```
nav {
    overflow: hidden;
    z-index: 100;
}
nav li { /* selects li in nav */
    display: inline-block;
    margin: 0;
    line-height: 56px;
}
nav a { /* selects a in nav */
    width: 100%;
    display: inline-block;
}
nav li:first-child { /* selects hamburger-button in nav */
    display: none;
}
```

#### JS
```
/* Create activateBurger function */
function activateBurger() {
    /*Grab the nav element*/
    let nav = document.getElementById("nav");
    /*Check if it isn't responsive-enabled yet
      (we add responsive to the class name if it is)*/
    if (nav.className != "responsive") {
        nav.className += "responsive";
    } else {
        nav.className = "";
    }
}
```

## With Social Media Icons
Use the code from the original, but add these modifications.
<p align="center">
  <img height="65px" src="https://user-images.githubusercontent.com/43857043/145661500-76fd194b-2251-4845-9a3f-fd1cad21552b.png">
</p>

#### HTML
Add `<li class="nav-icon-li">` The social media icon of your choice with a `class="fa nav-icon fa-SOCIALMEDIA"` attribute
```
<nav id="nav">
            <ul>
                <!-- The onclick event will activate our javascript function -->
                <li><a class="hamburger-button" onclick="activateBurger()">
                    <i class="hamburger fa fa-bars"></i>
                </a></li>
                <li><a href="#">Home</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#awards">Awards</a></li>
                <!-- Additions here!! -->
                <li class="nav-icon-li"><a href="#your-link" class="fa nav-icon fa-linkedin"></a></li>
                <li class="nav-icon-li"><a href="#your-link" class="fa nav-icon fa-envelope"></a></li>
            </ul>
        </nav>
```

#### CSS
```
nav .nav-icon {
    background-color: transparent;
    line-height: 56px;
    padding: 0px 18px;
}
.nav-icon-li {
    float: right;
    padding: 0px 6px;
}
```
