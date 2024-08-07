### Understanding Media Queries

Media queries are a powerful tool in CSS that allow you to apply styles based on certain conditions, such as the width or height of the viewport, the device orientation, and more. Here's a breakdown of the different components and techniques used in media queries.

#### 1. Basic Structure of a Media Query

A basic media query consists of:
- The `@media` rule.
- The type of media (e.g., `screen`).
- A condition (e.g., `max-width: 768px`).

```css
@media media-type and (condition) {
    /* CSS rules */
}
```

#### 2. Media Types

Media types specify the type of device the styles should apply to. The most common media types are:
- `screen`: Used for computer screens, tablets, smart-phones, etc.
- `print`: Used for printers.
- `all`: Suitable for all devices.

```css
@media screen and (max-width: 768px) {
    /* CSS rules for screens with a max-width of 768px */
}
```

#### 3. Conditions

Conditions in media queries define the circumstances under which the styles should be applied. These can include:
- `max-width`: Applies the styles if the viewport width is less than or equal to the specified value.
- `min-width`: Applies the styles if the viewport width is greater than or equal to the specified value.
- `max-height` and `min-height`: Similar to `max-width` and `min-width`, but for viewport height.
- `orientation`: Applies the styles based on the device orientation (`portrait` or `landscape`).

##### Examples:

- **Max-Width:**
  ```css
  @media (max-width: 768px) {
      body {
          background: blue;
      }
  }
  ```
  This applies styles when the viewport width is 768px or less.

- **Min-Width:**
  ```css
  @media (min-width: 769px) {
      body {
          background: green;
      }
  }
  ```
  This applies styles when the viewport width is 769px or more.

- **Combined Min-Width and Max-Width:**
  ```css
  @media (min-width: 769px) and (max-width: 1024px) {
      body {
          background: yellow;
      }
  }
  ```
  This applies styles when the viewport width is between 769px and 1024px.

#### 4. Using `only` and `not` Modifiers

- **`only`:** Ensures the styles are applied only if the entire query matches. This can help older browsers that do not support media queries to ignore the styles.
  ```css
  @media only screen and (max-width: 768px) {
      body {
          background: pink;
      }
  }
  ```

- **`not`:** Applies styles if the media query does not match.
  ```css
  @media not screen and (max-width: 768px) {
      body {
          background: purple;
      }
  }
  ```

#### 5. Practical Uses of Media Queries

- **Adapting Layouts:** You can change the layout of your site based on the device size.
  ```css
  @media (min-width: 768px) and (max-width: 1024px) {
      .sidebar {
          display: block;
      }
  }
  ```

- **Improving Readability:** Adjust font sizes for different devices to improve readability.
  ```css
  @media (max-width: 480px) {
      body {
          font-size: 14px;
      }
  }
  ```

- **Handling Orientation:** Apply styles based on whether the device is in portrait or landscape mode.
  ```css
  @media (orientation: landscape) {
      body {
          background: lightblue;
      }
  }
  ```

#### Example with Detailed Explanation

Let's look at a detailed example from the provided HTML and CSS code:

**HTML and CSS:**
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

**Explanation:**

1. **Default Styles:**
   - The `body` tag sets the default styles: `font-family`, `background`, `color`, `text-align`, and `padding-top`.
   - The `h1` elements are hidden by default (`display: none;`).

2. **Smartphones:**
   - `@media only screen and (max-width: 500px)` targets devices with a screen width of 500px or less.
   - The `only screen` part ensures this rule applies to screen devices only.
   - The body background changes to red, and the `#smartphone` heading is displayed.

3. **Tablets:**
   - `@media (min-width: 501px) and (max-width: 768px)` targets devices with a screen width between 501px and 768px.
   - The body background changes to blue, and the `#tablet` heading is displayed.

4. **Normal Desktops:**
   - `@media (min-width: 769px) and (max-width: 1200px)` targets devices with a screen width between 769px and 1200px.
   - The body background changes to green, and the `#normal` heading is displayed.

5. **Widescreens:**
   - `@media (min-width: 1201px)` targets devices with a screen width of 1201px or more.
   - The body background changes to black, and the `#widescreen` heading is displayed.

6. **Landscape Orientation:**
   - `@media (max-height: 500px)` targets devices where the viewport height is 500px or less, typically in landscape orientation.
   - The body background changes to orange, and the `#landscape` heading is displayed.

### Why Use Min and Max Together?

Using both `min-width` and `max-width` together allows you to target specific ranges of screen sizes. This is useful for creating breakpoints that ensure your design adapts smoothly across a variety of devices without abrupt changes.

**Example:**
```css
@media (min-width: 769px) and (max-width: 1024px) {
    body {
        background: yellow;
    }
}
```
- This query targets devices with a width between 769px and 1024px, applying styles specifically to tablets in landscape mode and smaller desktops.

### Why Specify Media Type (`screen`)?

Specifying the media type (e.g., `screen`) ensures that the styles are applied only to specific devices. This can be useful for differentiating styles between screens and printed documents.

**Example:**
```css
@media screen and (max-width: 768px) {
    body {
        background: lightblue;
    }
}
```
- This rule applies only to screen devices with a width of 768px or less, ignoring print media or other types.

By understanding these different ways to create media queries and their purposes, you can design more responsive and flexible websites that provide a better user experience across various devices and screen sizes.
