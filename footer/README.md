# Footer
<p align="center">
  <img height="175px" src="https://user-images.githubusercontent.com/43857043/145662078-8be5a08e-adbc-42d8-b543-607ab368e676.png">
</p>

The footer can contain contact information, your name, year, etc. This, like all other components here, is just an example.

Place this as the last element of your  `<body>` element in the HTML. 
This goes **outside and below** the `<div class="outer-container">` element.


#### HTML
```
<footer>
    <a class="footer-link" href="#">Back to Top</a>
    <p class="footer-text">Your name here. example.email@gmail.com</p>
    <p class="footer-text">December, 2021.</p>
</footer>
```

#### CSS
```
footer {
    margin: 40px 10px;
    text-align: center;
}

.footer-link {
    display: inline-block;
    text-decoration: none;
    color: teal;
    font-weight: bold;
    margin: 30px 0px;
}
.footer-text {
    margin: 20px 0px;
    color: gray;
    font-size: .75em;
}
```
