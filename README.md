# Sample-Portfolio-Components
A collection of web components for a portfolio page. Navigate the folders for component code and ask for help!

## Starting Code
Copy & paste this code into a file called `index.html`.
```
<!DOCTYPE html>
<html>
    <head>
        <meta content="width=device-width, initial-scale=1" name="viewport" />
        <script>

        </script>
        <style>
          body {margin: 0px;}
          .outer-container {
              margin: auto;
              display: flex;
              flex-direction: column;
              align-items: center;
          } 

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
        </style>
    </head>
    <body>
        <div class="outer-container">
            ## All your webpage elements go between the <body></body> tags. For styling, most elements will go in this #outer-container div
        </div>
    </body>
</html>
```
