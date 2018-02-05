# Seatwork 2

At the end of this exercise, you should learn: 

- How to implement several common web page layouts
- How to use web fonts
  
### Step 0. Plan ahead.

Plan to finish coding at 7:55 AM.

### Step 1. Fork the boilerplate project 

To get up to speed quickly, we'll start with a boilerplate HTML. Feel free to replace this with your own content if you prefer (and have the time). 

Log in to Github, open this repository: https://github.com/JBRC-ph/css-seatwork-2, and click the Fork link at the upper right portion of the page.

NOTE: You can work by directly editing the HTML and CSS file from Github.com. However, changes on your code can take a few minutes to propagate to Github Pages. I recommend cloning the repository locally and edit the web page using Visual Studio Code. After each CSS change, reload index.html in your browser to see how the CSS change affects the layout of the page.

### Step 2. Enable Github Pages for the project

This will let you open the HTML code in your browser as a web page, and not just as HTML code. For instructions on how to do this, see https://github.com/JBRC-ph/EmpowermentTechnologies/blob/master/github-pages-howto.md#5-enable-github-pages-for-the-project (skip to Step 5).

### Step 3. Test your workflow

Open your project. Make some changes in index.html. Reload the page in your browser, and verify that the change you made is reflected. 

This test ensures that the file you're editing is the same one you're testing :)

### Step 4. Work on Exercise 1.

On this step you will implement this layout:

![3-section-layout](https://github.com/JBRC-ph/EmpowermentTechnologies/blob/master/images/Body-3sections.png)

Follow these sub-steps for this exercise:

- Create a new file, `exercise1.html`, and copy the contents of `index.html` into it
- Open `exercise1.html` on your browser. Notice that the sections are already stacked on top of each other. HTML elements are stacked on top of each other by default.
- But just to be sure and to make the sections more visible, let's give them a background color. Add this to `style.css` and reload `exercise1.html` on the browser:

```
section.row {
    background-color: yellow;
}
```

### Step 5. Work on Exercise 2.

On this step you will implement this layout:

![3-column-layout](https://github.com/JBRC-ph/EmpowermentTechnologies/blob/master/images/Body-3columns.png)

Follow these sub-steps for this exercise:

- Create a new file, `exercise2.html`, and copy the contents of `index.html` into it
- Edit `index.html` and change the class of the section tags. Change the sections `<section class="row">` to `<section class="col">`
- Edit `style.css` and add a style for the columns:

```
section.col {
    width: 33%;
    float: left;
}
```

### Step 6. Work on Exercise 3.

On this step you will implement this layout:

![3-column-layout](https://github.com/JBRC-ph/EmpowermentTechnologies/blob/master/images/Combination.png)

Work on this as a homework and submit next week.

### Step 7. Upload to Github.

If you worked locally, upload your work to Github. You can view your work in https://yourusername.github.io/css-seatwork-2. Replace `yourusername` with your actual Github username.

- https://yourusername.github.io/css-seatwork-2/exercise1.html
- https://yourusername.github.io/css-seatwork-2/exercise2.html
- https://yourusername.github.io/css-seatwork-2/exercise3.html

Congratulations, you're done!

