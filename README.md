# Sample-Portfolio-Components
A collection of web components for a portfolio page. Navigate the folders for component code and ask for help!

## Starting Code
### index.html
Copy & paste this code into a file called `index.html`.
```
<!DOCTYPE html>
<html>
    <head>
        <!-- The head contains info about the webpage like title and styling -->
        <meta content="width=device-width, initial-scale=1" name="viewport" />
        <script src="script.js"></script>
        <link rel="stylesheet" href="style.css">
        <title>PLACE YOUR TITLE HERE</title>
    </head>
    <body>
        <!-- The body contains elements that will display on your webpage -->
        <main class="outer-container">
            ## All your webpage elements go between the body tags. For styling, most elements will go in this #outer-container main element
        </main>
    </body>
</html>
```
### style.css
Copy & paste this code into a file called `style.css`
```

body {
  margin: 0px;
  font-family: sans-serif;
  /* I recommend adding font-family: sans-serif; to the body{} style rule for a sleeker font*/
}

.outer-container {
  box-sizing: border-box ;
  margin: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
} 

/*Style rules not in a media query can go here, above the media queries*/

@media only screen and (max-width: 600px) {   /* For viewports smaller than 600px */
    .outer-container {
        width: 95%;
        justify-content: center;
    }
}

@media only screen and (min-width: 600px) {   /* For viewports 600px wide or larger */
    .outer-container {
        width: 80%;
        justify-content: center;
    }
}

@media only screen and (min-width: 1000px) {   /* For viewports 1000px wide or larger */
    .outer-container {
        width: 60%;
        justify-content: center;
    }
}
```
### script.js
Create a script.js 

There is no content in this file yet.
