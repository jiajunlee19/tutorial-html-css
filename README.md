# Introduction
This is a html-css tutorial, credits to [link](https://www.youtube.com/watch?v=uDkjZ-UjgX0&list=PLK5U0tyd34tBDtXeYW5hGyl8g_U3ex3wx).

Modify codes and open a live server on [index.html](/index.html).

<br>

# Basic HTML Structure
HTML is comprised of bunch of `elements`, you can simply generate them by typing `html-5` in [index.html](/index.html). Here's an example of the basic structure.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Title</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>This is a h1 heading</h1>
        <h2>This is a h2 heading</h2>
        <h3>This is a h3 heading</h3>
    </header>
    <main>
        <section>
            <p>This is a paragraph, with a <a href="/">link</a> and a <span>span</span> !</p>
        </section>
        <section>
            <ul>
                <li>unordered list 1</li>
                <li>unordered list 2</li>
                <li>unordered list 3</li>
            </ul>
        </section>
        <section>
            <button>This is a button</button>
            <img src="" alt="This is an image">
            <form>
                <input placeholder="This is an text input of a form">
                <textarea placeholder="This is an multiline text area of a form"></textarea>
            </form>
        </section>
    </main>
    <footer>
        This is a footer
    </footer>
</body>
</html>
```

<br>

# Basic CSS
In the previous Basic HTML example, there's just plain text with no style. We can use CSS to style them !

Styles can be defined in [style.css](/style.css). Here's an example:
```html
<section>
    <p id="p-blue-1">I'm styled by id #p-blue-1</p>
    <p class="p-red">I'm styled by class .p-red</p>
    <button id="b-1">I'm a styled button with paddings, margins and border</button>
</section>
```

```css
@keyframes fade-in {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}

#p-blue-1 {
    color: blue;
    font-size: medium;
    text-align: center;
}

.p-red {
    color: red;
}

#b-1 {
    display: block;
    padding: 30px; /*padding is the space between content to border*/
    margin: auto; /*margin is the space outside of border*/
    border: 10px solid black; /*margin-border-padding-content*/
    transform: scale(1);
    transform: rotate(360);
    transform: translate(0px, 0px); /*Offset by (x,y) coordinates*/
    transition: 0.4s; /*smoothen transition*/
    animation: fade-in 1s; /*animation with keyframes*/
}

#b-1:hover {
    transform: scale(2);
    cursor: pointer;
}

img {
    display: block; /*Make it a block which brings it over to next line*/
}
```

<br>

# Intermediate CSS
```html
<section class="intermediate-css">
    <h4 class="flexbox-title">Flex Box</h4>
    <div class="flexbox">
        <div class="box">1</div>
        <div class="box">2</div>
        <div class="box">3</div>
    </div>
</section>
```

```css
.intermediate-css {
    margin-top: 20px;
}

.flexbox {
    height: 300px;
    width: 600px;
    background-color: grey;

    display: flex;
    flex-direction: row;
    justify-content: start;
    align-items: start;
    position: relative; /*relative set it as a reference point*/
}

.box {
    height: 50px;
    width: 50px;
    background-color: yellow;
    text-align: center;
}

.box:nth-child(1) {
    background-color: var(--accent);

    position: absolute; /*absolute set an exact position independent of layout*/
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%); /*Offset it to center*/
}

:root {
    --accent: #0fddad; /*Creating global variables to be used by var(--name)*/
}

.flexbox-title::after {
    content: '';
    height: 5px;
    width: 75px;
    background-color: darkgoldenrod;
    display: block;
}
```

# Advanced Flex Box
Once we learnt thru all the basics, lets dive into an advanced layout, `Flex Box` !

Navigate to [flexbox/index.html](/flexbox/index.html)

<br>