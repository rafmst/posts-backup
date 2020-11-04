## Implementing Dark Mode without Javascript

Why do something like this? Well, its simple, just for the fun of it. You might arguee that everybody has scripts enabled in the browser and I agree with you, so, once again, I did this just for the fun of it and to show, what is to me, the best way to implement a dark mode toggler (in terms of stylesheets).

## Basic code

First things first. We need to create a boilerplate for testing the code. I'm using [CodePen](https://codepen.io) for this, I will leave a link for the entire project at the end. The basics that we need is an input, a label for that input and a container. Like this:

```html
<body>
    <input type="checkbox" id="toggleMode" />
    <label for="toggleMode" class="toggleDark">Dark Mode</label>
    <label for="toggleMode" class="toggleLight">Light Mode</label>
    <div id="container">
        <!-- your code should be here -->
    </div>
</body>
```

It is really important to have the input followed by the label on the top level of your html code. This way, everything inside the container can be changed.

## Using CSS variables

To achieve this we will use CSS variables in the root pseudo selector and we set our light mode colors first, because in this case, the light mode will be the default one.

```css
:root{
    --bg: #ffffff;
    --text: #000000;
}
```

The default light mode basically is a white background with black text, just a simple example to show how it's best done(in my opinion). In the end I will leave a project with a more complex example.

## Sibling and `:checked` selectors

As you may already guessed, we will use the `:checked` pseudo-selector to achieve the toggle effects. We need to differentiate the styles when the input is checked and when it isn't. By default when the input is not checked it means we are currently viewing the light mode, when it is checked we are suposed to view the dark mode.

```CSS
#toggleMode:checked ~ #container{
    --bg: #000000;
    --text: #FFFFFF;
}

#container{
    background-color: var(--bg);
}

p{
    color: var(--text);
}
```

This line of code basically means, when the `#toggleMode` is `checked` look for the next sibling with the id `container`. Now everything inside `#container` will have new variable values, because we are using it as our "body" tag. 

## Conclusion

I do find this to be the best way to implement a dark mode/light mode toggle in terms o CSS, but I would change the checkbox implementation with something simpler with javascript. As I said in the beginning this was just for fun, and check if it was possible. The complex example, as promised, is [here](https://codepen.io/rafaelsnts/pen/BEzZoX).