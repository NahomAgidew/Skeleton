# [Skeleton](http://getskeleton.com)
Skeleton is a simple, responsive boilerplate to kickstart any responsive project.

Check out <http://getskeleton.com> for documentation and details.

## Getting started

There are a couple ways to download Skeleton:
- [Download the zip](https://github.com/dhg/Skeleton/releases/download/2.0.4/Skeleton-2.0.4.zip)
- Clone the repo: `git clone https://github.com/dhg/Skeleton.git` (Note: this is under active development, so if you're looking for stable and safe, use the zipped download)

## Demo
This template is an example of how easy it can be to create a landing page with just the Skeleton grid and a few custom styles. The entire demo is ~150 lines of CSS including comments (most of which is positioning the phones at the top).
[Demo](http://getskeleton.com/examples/landing/)
[Source](https://github.com/dhg/Skeleton/tree/gh-pages/examples/landing)


### What's in the download?

The download includes Skeleton's CSS, Normalize CSS as a reset, a sample favicon, and an index.html as a starting point.

```
Skeleton/
├── index.html
├── css/
│   ├── normalize.min.css
│   └── skeleton.css
└── images/
    └── favicon.ico

```

### Why it's awesome

Skeleton is lightweight and simple. It styles only raw HTML elements (with a few exceptions) and provides a responsive grid. Nothing more.
- Around 400 lines of CSS unminified and with comments
- It's a starting point, not a UI framework
- No compiling or installing...just vanilla CSS


## Browser support

- Chrome latest
- Firefox latest
- Opera latest
- Safari latest
- IE latest

The above list is non-exhaustive. Skeleton works perfectly with almost all older versions of the browsers above, though IE certainly has large degradation prior to IE9.

## Is Skeleton for you?
You should use Skeleton if you're embarking on a smaller project or just don't feel like you need all the utility of larger frameworks. Skeleton only styles a handful of standard HTML elements and includes a grid, but that's often more than enough to get started.

## Documentation
### The Grid
The grid is a 12-column fluid grid with a max width of 960px, that shrinks with the browser/device at smaller sizes. The max width can be changed with one line of CSS and all columns will resize accordingly. The syntax is simple and it makes coding responsive much easier.

```
<!-- .container is main centered wrapper -->
<div class="container">

  <!-- columns should be the immediate child of a .row -->
  <div class="row">
    <div class="one column">One</div>
    <div class="eleven columns">Eleven</div>
  </div>

  <!-- just use a number and class 'column' or 'columns' -->
  <div class="row">
    <div class="two columns">Two</div>
    <div class="ten columns">Ten</div>
  </div>

  <!-- there are a few shorthand columns widths as well -->
  <div class="row">
    <div class="one-third column">1/3</div>
    <div class="two-thirds column">2/3</div>
  </div>
  <div class="row">
    <div class="one-half column">1/2</div>
    <div class="one-half column">1/2</div>
  </div>

</div>

<!-- Note: columns can be nested, but it's not recommended since Skeleton's grid has %-based gutters, meaning a nested grid results in variable with gutters (which can end up being *really* small on certain browser/device sizes) -->

```
### Typography
Type is set with the <code>rems</code>, so font-sizes and spacial relationships can be responsively sized based on a single <code>html</code> font-size property. Out of the box, Skeleton never changes the <code>html</code> font-size, but it's there in case you need it for your project. All measurements are still base 10 though so, an <code>h1</code> with <code>5.0rem</code> font-size just means <code>50px</code>.
The typography base is [Raleway](http://www.google.com/fonts/specimen/Raleway) served by Google, set at 15rem (15px) over a 1.6 line height (24px). Other type basics like anchors, strong, emphasis, and underline are all obviously included.
Headings create a family of distinct sizes each with specific <code>letter-spacing</code>, <code>line-height</code>, and <code>margins</code>.

```
<!-- Standard Headings -->
<h1>Heading</h1>
<h2>Heading</h2>
<h3>Heading</h3>
<h4>Heading</h4>
<h5>Heading</h5>
<h6>Heading</h6>

<!-- Base type size -->
<p>The base type is 15px over 1.6 line height (24px)</p>

<!-- Other styled text tags -->
<strong>Bolded</strong>
<em>Italicized</em>
<a>Colored</a>
<u>Underlined</u>
```

### Buttons
Buttons come in two basic flavors in Skeleton. The standard ```<button>``` element is plain, whereas the ```.button-primary``` button is vibrant and prominent. Button styles are applied to a number of appropriate form elements, but can also be arbitrarily attached to anchors with a ```.button``` class.

```
<!-- Standard buttons -->
<a class="button" href="#">Anchor button</a>
<button>Button element</button>
<input type="submit" value="submit input">
<input type="button" value="button input">

<!-- Primary buttons -->
<a class="button button-primary" href="#">Anchor button</a>
<button class="button-primary">Button element</button>
<input class="button-primary" type="submit" value="submit input">
<input class="button-primary" type="button" value="button input">
```

### Forms
Forms are a huge pain, but hopefully these styles make it a bit easier. All inputs, select, and buttons are normalized for a common height cross-browser so inputs can be stacked or placed alongside each other.
```
<!-- The above form looks like this -->
<form>
  <div class="row">
    <div class="six columns">
      <label for="exampleEmailInput">Your email</label>
      <input class="u-full-width" type="email" placeholder="test@mailbox.com" id="exampleEmailInput">
    </div>
    <div class="six columns">
      <label for="exampleRecipientInput">Reason for contacting</label>
      <select class="u-full-width" id="exampleRecipientInput">
        <option value="Option 1">Questions</option>
        <option value="Option 2">Admiration</option>
        <option value="Option 3">Can I get your number?</option>
      </select>
    </div>
  </div>
  <label for="exampleMessage">Message</label>
  <textarea class="u-full-width" placeholder="Hi Dave …" id="exampleMessage"></textarea>
  <label class="example-send-yourself-copy">
    <input type="checkbox">
    <span class="label-body">Send a copy to yourself</span>
  </label>
  <input class="button-primary" type="submit" value="Submit">
</form>

<!-- Always wrap checkbox and radio inputs in a label and use a <span class="label-body"> inside of it -->

<!-- Note: The class .u-full-width is just a utility class shorthand for width: 100% -->
```

### Lists
```
<ul>
  <li>Item 1</li>
  <li>
    Item 2
    <ul>
      <li>Item 2.1</li>
      <li>Item 2.2</li>
    </ul>
  </li>
  <li>Item 3</li>
</ul>

<!-- Easily substitute any <ul> or an <ol> to get number lists or sublists. Skeleton doesn't support lists nested deeper than 2 levels -->
```

### Code
Code styling is kept basic – just wrap anything in a ```<code>``` and it will appear like this. For blocks of code, wrap a ```<code>``` with a ```<pre>```.

```
<pre>
  <code>
    .some-class {
      background-color: red;
    }
  </code>
</pre>

<!-- Remember every whitespace and break will be preserved in a <pre>, including indentation in your code -->
```

### Tables
Be sure to use properly formed table markup with ```<thead>``` and ```<tbody>``` when building a ```table```.
```
<table class="u-full-width">
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
      <th>Sex</th>
      <th>Location</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Dave Gamache</td>
      <td>26</td>
      <td>Male</td>
      <td>San Francisco</td>
    </tr>
    <tr>
      <td>Dwayne Johnson</td>
      <td>42</td>
      <td>Male</td>
      <td>Hayward</td>
    </tr>
  </tbody>
</table>
```

### Media Queries
Skeleton uses media queries to serve its scalable grid, but also has a list of queries for convenience of styling your site across devices. The queries are mobile-first, meaning they target ```min-width```. Mobile-first queries are how Skeleton's grid is built and is the preferrable method of organizing CSS. It means all styles outside of a query apply to all devices, then larger devices are targeted for enhancement. This prevents small devices from having to parse tons of unused CSS. The sizes for the queries are:
* Desktop HD: 1200px
* Desktop: 1000px
* Tablet: 750px
* Phablet: 550px
* Mobile: 400px

```
/* Mobile first queries */

/* Larger than mobile */
@media (min-width: 400px) {}

/* Larger than phablet */
@media (min-width: 550px) {}

/* Larger than tablet */
@media (min-width: 750px) {}

/* Larger than desktop */
@media (min-width: 1000px) {}

/* Larger than Desktop HD */
@media (min-width: 1200px) {}
```

### Utilities
Skeleton has a number of small utility classes that act as easy-to-use helpers. Sometimes it's better to use a utility class than create a whole new class just to float an element.

```
/* Utility Classes */

/* Make element full width */
.u-full-width {
  width: 100%;
  box-sizing: border-box; }

/* Make sure elements don't run outside containers (great for images in columns) */
.u-max-full-width {
  max-width: 100%;
  box-sizing: border-box; }

/* Float either direction */
.u-pull-right {
  float: right; }
.u-pull-left {
  float: left; }

/* Clear a float */
.u-cf {
  content: "";
  display: table;
  clear: both; }
```

## License

All parts of Skeleton are free to use and abuse under the [open-source MIT license](https://github.com/dhg/Skeleton/blob/master/LICENSE.md).

## Colophon

Skeleton was built using [Sublime Text 3](http://www.sublimetext.com/3) and designed with [Sketch](http://bohemiancoding.com/sketch). The typeface [Raleway](http://www.google.com/fonts/specimen/Raleway) was created by [Matt McInerney](http://matt.cc/) and [Pablo Impallari](http://www.impallari.com/). Code highlighting by Google's [Prettify library](https://code.google.com/p/google-code-prettify/). Icons in the header of the documentation are all derivative work of icons from [The Noun Project](http://thenounproject.com). [Feather](http://thenounproject.com/term/feather/22073) by Zach VanDeHey, [Pen](http://thenounproject.com/term/pen/21163) (with cap) by Ed Harrison, [Pen](http://thenounproject.com/term/pen/32847) (with clicker) by Matthew Hall, and [Watch](http://thenounproject.com/term/watch/48015) by Julien Deveaux.


## Acknowledgement

Skeleton was originally created by [Dave Gamache](https://twitter.com/dhg) for a better web.
This repository is maintained by [Nahom Abi](https://twitter.com/mdnahom)
