# Bootstrap CSS

![](https://www.opensourcevarsity.com/wp-content/uploads/2016/07/bootstrap-logo-2.png)

### Learning Objectives

* Require Bootstrap into your project
* Understand and implement a grid system
* Design HTML pages with the aid of Bootstrap

## Why Bootsrap

Bootsrap was created by Twitter and open sourced in 2011. Since then, it has been at, or near the top of the charts in terms of use and popularity. 

It is a heavy-weight framework, meaning you need to include a pretty large file to use it, but it can do a LOT for developers. 

Until recently, I preferred light-weight CSS frameworks like Skeleton.CSS. However, since CSS Grid has been implemented, there isn't a lot of point to it anymore! Skeleton offers a grid plus a few utility classes. Bootstrap offers both of those, and also a lot of great components, and more. Let's dig in!

## Intro to Bootstrap

* [Bootstrap](http://getbootstrap.com/) is a **css library** created by a small team of developers at Twitter and maintained by a much larger community of contributors.
* The framework consists of one main CSS file, an optional theme CSS file, and an optional JS file.

Bootstrap is extremely popular and knowledge of at least one CSS framework is a very valuable skill to have (and totally worth putting on your resume). 

Bootstrap comes with a ton of features, including:

- Responsive Grid System based on Flexbox
- CSS library for quick and easy styling
- UI components - HTML + CSS 
  - navigation
  - buttons
  - forms
  - etc.
- Javascript widgets to make your page interactive
- Tons more

## Sites Using Bootstrap

* [Instacart](https://www.instacart.com/)
* [Vogue](https://www.vogue.mx/?international)
* [Lyft](https://www.lyft.com/)

## Including Bootstrap with HTML
* To use Bootstrap, we need to include Bootstrap's CSS library, optional Javascript libraries (+ or - an optional Bootstrap-Theme CSS file).
* We also need to include jQuery, as Bootstrap's JS plug-ins depend on it.  
* There are a few different ways to accomplish this, listed below. In this class, we'll keep it simple and stick with the CDN.

1. CDN (Content Delivery Network - someone else hosts the library/framework and you access it via a URL):  [http://getbootstrap.com/getting-started/#download-cdn](http://getbootstrap.com/getting-started/#download-cdn). Where do we include these in our HTML file?
2. Download the actual CSS and JS files and link to them on your local computer - better for offline/local development

## Responsive Grid System
* Columns are written in the following format as a class attribute: `col-(breakpoint)-(offset)`
* For example: `col-sm-4`
* Columns are often wrapped into an element with a class of `row` or `container`.

![](https://cdn-images-1.medium.com/max/800/1*9nkJt3S1Fe_KMkDtpIhgXw.png)

#### Start with a container
To ensure all your Bootstrap styles behave properly, always put your content inside an element with a class "container" (usually `<div class="container">`). This will center your content and leave a small margin on the sides of the page. If you would like to use the full width of the screen (no margin) use `class="container-fluid"`

#### Page layout using the Grid System
Bootstrap's grid system is based on the idea that a page layout for any given screen size is represented with 12 fluid **columns**.  Columns are always horizontally contained in **rows**, which in turn are contained inside of the previously mentioned `container` (container > row > column):

The grid will default to making each column the same width. Create a div with class "row" and put divs with class "col" in in. The Bootstrap grid will automatically make them all equal width:

  ``` html
   <div class="row">
    <div class="col">col</div>
    <div class="col">col</div>
    <div class="col">col</div>
  </div>
  ```

Or, specify how big each column should be with "col-" classes. The number after the hyphen represents how many segments out of 12 the column should take up:

   ``` html
   <div class="row">
    <div class="col-3">col-3</div>
    <div class="col-6">col-6</div>
    <div class="col-3">col-3</div>
  </div>
  ```
The above code will make the middle column twice as large as the outer two.

For other examples, check out the [Bootstrap docs](http://getbootstrap.com/css/#grid)  

## Breakpoints

However you define your columns, Bootstrap's grid is responsive by default. So on mobile, it will collapse the columns into a singe item per row! 

You can also give the grid additional breakpoints. For example, you can make a 6 column grid become two columns on a tablet!

## Typography
For a complete list: [Bootstrap Typography classes](http://getbootstrap.com/css/#type)

To align text, use these classes.  

``` html
 <p class="text-left">Left aligned text.</p>
 <p class="text-center">Center aligned text.</p>
 <p class="text-right">Right aligned text.</p>
 <p class="text-justify">Justified text.</p>
 <p class="text-nowrap">No wrap text.</p>
```
More useful typography classes...

``` html
 <p class="lead">This text will stand out in a paragraph</p>
 <small>This line of text is meant to be treated as fine print.</small>
 <p class="text-lowercase">Lowercased text.</p>
 <p class="text-uppercase">Uppercased text.</p>
 <p class="text-capitalize">Capitalized text.</p>
```


## Icons
![](https://coreui.io/assets/img/blog/bootstrap-icons.jpg)

Bootstrap comes with a set of icons that can be included in your page using the `<i></i>` tag. Check out these icons [here](http://getbootstrap.com/components/#glyphicons)

## Buttons
![](https://getbootstrap.com/docs/3.4/examples/screenshots/theme.jpg)

Bootstrap provides a wide selection of button sizes and colors.  Button classes can be applied not just to `<button>` elements, but also `<a>` and `<input>` elements

Sometimes you need to provide multiple classes to an element in order for Bootstrap to style it.  The button classes are an example of this:

``` html
 <!-- Standard button -->
 <button type="button" class="btn btn-default">Default</button>
 
 <!-- Provides extra visual weight and identifies the primary action in a set of buttons -->
 <button type="button" class="btn btn-primary">Primary</button>
 
 <!-- Contextual button for informational alert messages -->
 <button type="button" class="btn btn-info">Info</button>

 <!-- Indicates caution should be taken with this action -->
 <button type="button" class="btn btn-warning">Warning</button>
```  
... and so on.  See the [docs](http://getbootstrap.com/css/#buttons) for a comprehensive list of options.  Note you can add a third class denoting size to any of the above: `.btn-lg`, `.btn-sm`, `.btn-xs`


## Images 
![](http://webseotips.com/wp-content/uploads/2017/12/Screenshot-221.jpg)

Bootstrap helps you format images using `class="img-rounded"` (rounds the corners), `class="img-circle"` (makes the image a circle) and `class="img-thumbnail"` (adds a border). You can also add a `class="img-responsive"` to your image to make it scale well when the screen size changes (this sets its max-width to 100% of its parent element and the height to auto for maintaining aspect)

## Forms
![](https://www.codeply.com/img/JVP2nxfv0p)
Bootstrap is also very helpful when you need to style your forms. All textual `<input>`, `<textarea>`, and `<select>` elements with `class="form-control"` are set to width: 100% by default. Wrap labels and their associated controls (inputs) in `class="form-group"` for optimum spacing. 
 

## Javascript plug-ins
Bootstrap allows you to incorporate interactive behavior into your page with Javascript plug-ins.  We don't have time to get into this now, but lets take a quick look at some examples:

- [Responsive Nav bars](http://getbootstrap.com/components/#navbar)
- [Dropdowns](http://getbootstrap.com/javascript/#dropdowns)
- [Popovers](http://getbootstrap.com/javascript/#popovers)
- [Modals](http://getbootstrap.com/javascript/#modals)
- [Carousels](http://getbootstrap.com/javascript/#carousel)


## Resources

* [Bootsrap Docs](https://getbootstrap.com/docs/4.1/getting-started/introduction/)
* [50 min Boostrap Video Tutorial](https://www.youtube.com/watch?v=hnCmSXCZEpU)
* [Free Code Camp 30 Min Tutorial](https://www.freecodecamp.org/news/learn-bootstrap-4-in-30-minute-by-building-a-landing-page-website-guide-for-beginners-f64e03833f33/)
* [10 Part Video Course](https://scrimba.com/g/gbootstrap4)
* [Article: CSS Frameworks vs CSS Grid](https://www.smashingmagazine.com/2018/11/css-frameworks-css-grid/)
* [Article: 6 Popular CSS Frameworks](https://scotch.io/bar-talk/6-popular-css-frameworks-to-use-in-2019)
