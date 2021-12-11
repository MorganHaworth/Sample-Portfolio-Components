# Buttons and Links

Please reach out if something isn't working like you think it should - or if you want alterations. Or even if you have more ideas and want to know how to do them!

All of these components go inside the `<main class="outer-container">` element.

## Social Media Icons [Square and Circle]
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/145339040-b306b82d-ff2e-4cd7-bf78-02c6d12cc73c.png">
</p>

List of some available icons: fa-linkedin, fa-envelope, fa-github, fa-twitter, fa-stack-overflow, fa-facebook, fa-google, fa-youtube, fa-instagram, fa-pinterest, fa-skype

#### HTML

If not already present, add this `<link>` element inside the `<head></head>`.
```
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
```
Add this in `<main class="outer-container">` element. If you want a specific icon, add a `<a>` element with the `class` attribute value set to `fa fa-ICON_NAME`. When styling, set the `background:` attribute to the logo's color.
```
<div class="icon-container">
    <a href="#your-link" class="icon fa fa-linkedin"></a>
    <a href="#your-link" class="icon fa fa-envelope"></a>
    <a href="#your-link" class="icon fa fa-github"></a>
    <a href="#your-link" class="icon fa fa-twitter"></a>
</div>
```

#### CSS
```
.icon-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
.icon {
    padding: 20px;
    font-size: 30px;
    width: 30px;
    text-align: center;
    text-decoration: none;
    margin: 5px 5px;
    /* border-radius: 50%;  Add this declaration for circle icons*/
}
```
```
.fa-twitter {
    background: #55ACEE; /* Official logo color */
    color: white;
}
.fa-linkedin {
    background: #007bb5; /* Official logo color */
    color: white;
}
.fa-github {
    background: #333; /* Official logo color */
    color: white;
}
.fa-envelope {
    background: #BB001B; /* Gmail logo color */
    color: white;
}
```

## Download (Resume) File Button
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/145326216-2302bea8-a5cb-4f41-aa3e-94b0979c29d1.png">
</p>

Users are directed to new tab to view (and download) a file. Replace `assets/Resume.pdf` with the name of your file.
#### HTML
```
<a target="_blank" class="resume-link" href="assets/Resume.pdf">View Resume</a>
```
#### CSS
```
.resume-link {
    display: block;
    background: rgb(226, 226, 226); /* Color of button: Change this to a color you like */
    padding: 20px 30px;
    border-radius: 15px;
    border: none;
    box-shadow: 0px 4px 5px 0px lightgray;
    margin: 25px auto;
    box-sizing: border-box;
    font-weight: bold;
    text-align: center;
    font-size: 1.2em;
    text-decoration: none;
    color: rgb(50,50,50); /* Font color: Change this to a color you like */
}
.resume-link:hover {
    box-shadow: 0px 4px 5px 0px darkgray;
}
```
##### @media only screen and (max-width: 600px)
```
.resume-link {
    width: 100%;
}
```
