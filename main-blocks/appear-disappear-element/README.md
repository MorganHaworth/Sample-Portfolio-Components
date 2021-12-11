# Appearing and Disappearing Element

Please reach out if something isn't working like you think it should - or if you want alterations. Or even if you have more ideas and want to know how to do them!

This component goes inside the `<main class="outer-container">` element.

This show/hide concept can be applied to any element(s).

## Courses Example
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/145681199-93622703-02e3-4102-8649-c35b0cf72b2f.png">
</p>

#### HTML
The relevant elements are the `div` with `id="show-hide-courses` and `p` elements with `onclick=func()` attributes.
```
<div class="section-content">
    <div class="sc-heading">
        <span class="position">BS Civil Engineering</span>
        <span class="time">May 2009 - June 2012</span>
    </div>
    <p class="sc-location">3.2 GPA</p>
    <p class="sc-description">
        Participated in leadership groups.
    </p>
</div>
<div id="show-hide-courses">
    <!-- Anything you want can go in this div-->
    <!-- All that matters is you have an id you can select to style invisible and visible-->
    <ul>
        <li>Intro to Geomatics</li>
        <li>Theoretical Fluid Mechanics</li>
        <li>Water/Waste Water Treatment</li>
        <li>Structural Analysis</li>
        <li>Engineering Hydrology</li>
    </ul>
</div>
<p onclick="showCourses()" id="show-courses-indicator">
    Show courses <span><i class="fa fa-arrow-down"></i></span>
</p>
<p onclick="hideCourses()" id="hide-courses-indicator">
    Hide courses <span><i class="fa fa-arrow-up"></i></span>
</p>
```

#### CSS
```
#show-hide-courses {
    width: 100%;
    margin: 0px;
}
```

#### JS
```
function showCourses() {
    let courses = document.getElementById("show-hide-courses");
    courses.style.display = "block";
    let showCoursesIndicator = document.getElementById("show-courses-indicator");
    showCoursesIndicator.style.display = "none";
    let hideCoursesIndicator = document.getElementById("hide-courses-indicator");
    hideCoursesIndicator.style.display = "block";
}
function hideCourses() {
    let courses = document.getElementById("show-hide-courses");
    courses.style.display = "none";
    let showCoursesIndicator = document.getElementById("show-courses-indicator");
    showCoursesIndicator.style.display = "block";
    let hideCoursesIndicator = document.getElementById("hide-courses-indicator");
    hideCoursesIndicator.style.display = "none";
}
```
##### Add in window.onload function
```
let courses = document.getElementById("show-hide-courses");
courses.style.display = "none";
let hideCoursesIndicator = document.getElementById("hide-courses-indicator");
hideCoursesIndicator.style.display = "none";
```
