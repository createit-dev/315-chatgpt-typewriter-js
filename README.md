# Typing Like ChatGPT: A Simple JavaScript Typewriter Effect

This repository contains a simple and dynamic typewriter effect inspired by OpenAI's ChatGPT. The effect can be applied to both table content and regular text elements.

![Typewriter-ChatGPT-demo.gif](img%2FTypewriter-ChatGPT-demo.gif)

## Demo
A live demo of the effect can be seen:
https://createit-dev.github.io/315-chatgpt-typewriter-js/

## Features

- Pure JavaScript - no external libraries required (apart from the optional Bootstrap for styling).
- Can be applied to table cells (`<th>` and `<td>`) and regular text elements (`<p>`, `<span>`, and `<h1>`).
- Dynamic typing animation with adjustable speed.

## Usage

1. Include the script in your HTML:

```html
<script src="chatgpt-typewriter-js.js"></script>
```

2. Add the content you want to animate within an element with the ID `typewriter-gpt-1` for tables or `typewriter-gpt-2` for regular text elements.

3. Initialize JS
To activate the typewriter effect on your content, you need to call the script after the page has loaded.

Place the following script at the end of your HTML body:

```html
<script>
    window.onload = function() {

        // For tables
        const tables = document.querySelectorAll('#typewriter-gpt-1 table');
        tables.forEach(table => {
            const cells = Array.from(table.querySelectorAll('th, td'));
            if (cells.length) {
                typeTableContent(cells);
            }
        });

        // For normal text elements
        const textElements = Array.from(document.querySelectorAll('#typewriter-gpt-2 p, #typewriter-gpt-2 span, #typewriter-gpt-2 h1'));
        if (textElements.length) {
            typeTableContent(textElements);
        }
    }
</script>
```

4. Load your page and watch the typewriter effect in action!


## Example

The following is an example of how the script can be implemented:

```html
<div id="typewriter-gpt-2">
    <h1>Typing Like ChatGPT: A Simple JavaScript Typewriter Effect Tutorial</h1>
    <p>Revive 1909 Year in History using ChatGPT's Typing Animation in <span>pure Javascript</span></p>
</div>

<div id="typewriter-gpt-1">
    <table>
        <!-- table content -->
    </table>
</div>
```

## Customization

To adjust the typing speed, modify the `typingSpeed` constant in the script.


