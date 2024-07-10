### Student Guide: Understanding Media Queries in Responsive Design

This guide will help you understand how to use media queries to create responsive web designs. We will use the provided example to explain the code and demonstrate how media queries work.

#### Example HTML and CSS Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Media Queries</title>
    <style>
        body {
            font-family: Arial, Helvetica, sans-serif;
            background: gray;
            color: white;
            text-align: center;
            padding-top: 100px;
        }

        h1 {
            display: none;
        }

        /* Smartphones */
        @media only screen and (max-width: 500px) {
            body {
                background: red;
            }

            #smartphone h1 {
                display: block;
            }
        }

        /* Tablet */
        @media(min-width: 501px) and (max-width: 768px) {
            body {
                background: blue;
            }

            #tablet h1 {
                display: block;
            }
        }

        /* Normal */
        @media(min-width: 769px) and (max-width: 1200px) {
            body {
                background: green;
            }

            #normal h1 {
                display: block;
            }
        }

        /* Widescreen */
        @media(min-width: 1201px) {
            body {
                background: black;
            }

            #widescreen h1 {
                display: block;
            }
        }

        /* Landscape */
        @media(max-height: 500px) {
            body {
                background: orange;
            }

            #landscape h1 {
                display: block;
            }
        }
    </style>
</head>
<body>
    <div id="widescreen"><h1>Widescreen</h1></div>
    <div id="normal"><h1>Normal</h1></div>
    <div id="tablet"><h1>Tablet</h1></div>
    <div id="smartphone"><h1>Smartphone</h1></div>
    <div id="landscape"><h1>Landscape</h1></div>
</body>
</html>
```

#### Explanation of the Code

1. **Basic HTML Structure:**
   - The `<!DOCTYPE html>` declaration defines the document as HTML5.
   - The `<html lang="en">` tag sets the language of the document to English.
   - The `<meta charset="UTF-8">` tag specifies the character encoding for the document.
   - The `<meta name="viewport" content="width=device-width, initial-scale=1.0">` tag sets the viewport to ensure the page is rendered correctly on different devices.
   - The `<meta http-equiv="X-UA-Compatible" content="ie=edge">` tag ensures compatibility with Internet Explorer.
   - The `<title>Media Queries</title>` sets the title of the page.

2. **CSS Styling:**
   - The `body` tag sets the default styles for the page, including font family, background color, text color, text alignment, and padding.
   - The `h1` tag is initially set to `display: none;` to hide all headings by default.

3. **Media Queries:**
   Media queries are used to apply different styles based on the screen size and orientation. Each media query in this example changes the background color of the page and displays a specific heading based on the screen size or orientation.

   - **Smartphones:**
     ```css
     @media only screen and (max-width: 500px) {
         body {
             background: red;
         }
         #smartphone h1 {
             display: block;
         }
     }
     ```
     This media query applies when the screen width is 500px or less. The background color changes to red, and the "Smartphone" heading is displayed.

   - **Tablets:**
     ```css
     @media(min-width: 501px) and (max-width: 768px) {
         body {
             background: blue;
         }
         #tablet h1 {
             display: block;
         }
     }
     ```
     This media query applies when the screen width is between 501px and 768px. The background color changes to blue, and the "Tablet" heading is displayed.

   - **Normal:**
     ```css
     @media(min-width: 769px) and (max-width: 1200px) {
         body {
             background: green;
         }
         #normal h1 {
             display: block;
         }
     }
     ```
     This media query applies when the screen width is between 769px and 1200px. The background color changes to green, and the "Normal" heading is displayed.

   - **Widescreen:**
     ```css
     @media(min-width: 1201px) {
         body {
             background: black;
         }
         #widescreen h1 {
             display: block;
         }
     }
     ```
     This media query applies when the screen width is 1201px or more. The background color changes to black, and the "Widescreen" heading is displayed.

   - **Landscape:**
     ```css
     @media(max-height: 500px) {
         body {
             background: orange;
         }
         #landscape h1 {
             display: block;
         }
     }
     ```
     This media query applies when the screen height is 500px or less, typically for landscape orientation on smaller screens. The background color changes to orange, and the "Landscape" heading is displayed.

#### How to Test Media Queries

To see how media queries work, you can:
1. Resize your browser window to see the background color and headings change based on the screen width.
2. Use the developer tools in your browser (usually accessed by pressing `F12` or right-clicking and selecting "Inspect") to simulate different screen sizes and orientations.

This example demonstrates how to use media queries to create a responsive design that adjusts to different devices and orientations, enhancing the user experience across various platforms.
