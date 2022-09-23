<h1 align="center">
  <br>
  Hori<span color="#d9dcd6">seo<span>n
  <br>
</h1>

<h3 align="center">A website providing solutions to help your business grow</h3>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#accessibility-changes">Accessibility Changes</a> •
  <a href="#usage">Usage</a> •
  <a href="#credits">Credits</a>
</p>

![website screenshot](./assets/images/horiseon-website-demo.png)

## Key Features 

### Search Engine Optimization
The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.

### Online Reputation Management
The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.

### Social Media Marketing
Social media continues to have a sizable influence on buying habits. Social media marketing helps you determine which platforms are suited to your brand, using analytics to find the right markets and increase your lead generation.

### Lead Generation
Inbound strategies for lead generation require less work for your business, bringing customers directly to your website.

### Brand Awareness
Users find your business through paid and organic searches, increasing the search ranking and visibility for your business.

### Cost Management
As the search ranking for your business increases, your advertising costs decrease, and you no longer need to advertise your page.

## Accessibility Changes
At Horiseon, we strive to make our technology more accessible. The following changes were made over the previous version of the website:

### Semantic HTML
Semantic HTML elements clearly define their content. They are preferable to use over the more generic div tag, as it's easier to identify their function. The following changes were made to make Horiseon more semantically appropriate:

- Changed <code>&lt;div class="header"&gt;</code> to <code>&lt;header&gt;</code>
- Changed the <code>&lt;div&gt;</code> under the <code>&lt;h1&gt;</code> heading to <code>&lt;nav&gt;</code>
- Changed <code>&lt;div class="hero"&gt;</code> to <code>&lt;figure class="hero"&gt;</code>
- Changed <code>&lt;div class="content"&gt;</code> to <code>&lt;main&gt;</code>, since this is where the bulk of the visual space of the website is.
- Changed <code>&lt;div class="search-engine-optimization"&gt;</code> to <code>&lt;figure id="search-engine-optimization" class="solution"&gt;</code>. I also wrapped a <code>&lt;figcaption&gt;</code> around the header and caption describing the image.
- Changed <code>&lt;div id="online-reputation-management" class="online-reputation-management"&gt;</code> to <code>&lt;figure id="online-reputation-management" class="solution"&gt;</code>. I also wrapped a <code>&lt;figcaption&gt;</code> around the header and caption describing the image.
- Changed <code>&lt;div id="social-media-marketing" class="social-media-marketing"&gt;</code> to <code>&lt;figure id="social-media-marketing" class="solution"&gt;</code>. I also wrapped a <code>&lt;figcaption&gt;</code> around the header and caption describing the image.
- Changed <code>&lt;div class="benefits"&gt;</code> to <code>&lt;aside class="benefits"&gt;</code>. Since this content is on the side of the main content and tangentially related to the main content, I thought an <code>&lt;aside&gt;</code> element was the most appropriate.
- Changed <code>&lt;div class="benefit-lead"&gt;</code> to <code>&lt;section class="benefit"&gt;</code>. I also wrapped the child <code>&lt;img&gt;</code> and captions of this <code>&lt;section&gt;</code> in a <code>&lt;figcaption&gt;</code>.
- Changed <code>&lt;div class="benefit-brand"&gt;</code> to <code>&lt;section class="benefit"&gt;</code>. I also wrapped the child <code>&lt;img&gt;</code> and captions of this <code>&lt;section&gt;</code> in a <code>&lt;figcaption&gt;</code>.
- Changed <code>&lt;div class="benefit-cost"&gt;</code> to <code>&lt;section class="benefit"&gt;</code>. I also wrapped the child <code>&lt;img&gt;</code> and captions of this <code>&lt;section&gt;</code> in a <code>&lt;figcaption&gt;</code>.
- Changed <code>&lt;div class="footer"&gt;</code> to <code>&lt;footer&gt;</code>

### Logical HTML without Styling
HTML should provide the structure of a webpage and CSS should provide the styling. Reducing the amount of styling in the html document should make it easier to read. The following change was made to reduce the styling in html:

In the original index.html file, each solution element appeared like this:
```HTML
<div id="online-reputation-management" class="online-reputation-management">
  <img src="./assets/images/online-reputation-management.jpg" class="float-right" />
  <h2>Online Reputation Management</h2>
  <p>
      The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
  </p>
</div>
```

I felt like calling the class float-right to make it float-right was kind of indirectly using html to style and element, so I removed it.
It now appears like this:
```HTML
<figure id="online-reputation-management" class="solution">
  <img src="./assets/images/online-reputation-management.jpg" alt="A graph on a laptop showing your reputation increasing."/>
  <figcaption>
    <h2>Online Reputation Management</h2>
    <p>
      The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
    </p>
  </figcaption>
</figure>
```

### Accessible Alt Attributes
Screen readers read the output of a website. It's important alt attributes are defined so that screen readers will properly read an image and disabled folks can enjoy any website. The following changes were made to make images more accessible:

I added alt attributes to each image:
```HTML
<img src="./assets/images/digital-marketing-meeting.jpg" alt="Teammates collaborating.">
```
```HTML
<img src="./assets/images/search-engine-optimization.jpg" alt="A notepad with 'SEO' written on it."/>
```
```HTML
<img src="./assets/images/online-reputation-management.jpg" alt="A graph on a laptop showing your reputation increasing."/>
```
```HTML
<img src="./assets/images/social-media-marketing.jpg" alt="Several people at a table tweeting things, liking things on facebook, and watching media."/>
```
```HTML
<img src="./assets/images/lead-generation.png" alt="A gear with an arrow pointing downward, toward money."/>
```
```HTML
<img src="./assets/images/brand-awareness.png" alt="A light bulb"/>
```
```HTML
<img src="./assets/images/cost-management.png" alt="A gear with some money"/>
```

### Heading Attributes in Sequential Order
There should only be 1 h1 header, the next header should be an h2, and one shouldn't use h3 unless it's a subheader of an h2. It's good practice. The following changes were made to facilitate that:

For each section element with a class of "benefit", the original html looked like this (note the h3):
```HTML
<div class="benefit-lead">
  <h3>Lead Generation</h3>
  <img src="./assets/images/lead-generation.png" />
  <p>
    Inbound strategies for lead generation require less work for your business, bringing customers directly to your website.
  </p>
</div>
```

Since the <code>&lt;h3&gt;</code> tag isn't a subheader of any <code>&lt;h2&gt;</code> tag, it should be an <code>&lt;h2&gt;</code>, so I switched it
to an <code>&lt;h2&gt;</code> element and increased the size of the font in the css file to 20 pixels. Each benefit now looks like this:
```HTML
<section class="benefit">
  <h2>Brand Awareness</h2>
  <figure>
    <img src="./assets/images/brand-awareness.png" alt="A light bulb"/>
    <figcaption>
      <p>
        Users find your business through paid and organic searches, increasing the search ranking and visibility for your business.
      </p>
    </figcaption>
  </figure>
</section>
```

### Concise, Descriptive Title
Each website should have a short, descriptive title so that people know where they are navigating to. The title was "website", now it looks like this:
```HTML
<title>Horiseon Social Solution Services</title>
```

### Links All Function Correctly
All the links in a website should work.

In the original index.html, the search-engine-optimization element didn't have an id:
```HTML
<div class="search-engine-optimization">
  <img src="./assets/images/search-engine-optimization.jpg" class="float-left" />
  <h2>Search Engine Optimization</h2>
  <p>
    The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
  </p>
</div>
```

Because of that, our navigation link didn't work correctly, as it needs an element with the id of search-engine-optimization to jump to:
```HTML
<a href="#search-engine-optimization">Search Engine Optimization</a>
```

So, I added an id to the search-engine-optimization element so the link now works:
```HTML
<figure id="search-engine-optimization" class="solution">
```

### CSS Consolidation
The amount of code should be a minimum in any project/website in order to reduce reduncancy and make values easy to read/change. A minimum amount of code makes our code easy to read and modify. The following changes were made to consolidate CSS code in style.css:

Originally, there were three different classes of benefit:
```CSS
.benefit-lead {
    margin-bottom: 32px;
    color: #ffffff;
}

.benefit-brand {
    margin-bottom: 32px;
    color: #ffffff;
}

.benefit-cost {
    margin-bottom: 32px;
    color: #ffffff;
}

```

Since these all do the same things, I consolidated all of this into one selector:
```CSS
.benefit {
    margin-bottom: 32px;
    color: #ffffff;
}
```
The same goes for the header and image inside each benefit. The code originally looked like this:
```CSS
.benefit-lead h3 {
    margin-bottom: 10px;
    text-align: center;
}

.benefit-brand h3 {
    margin-bottom: 10px;
    text-align: center;
}

.benefit-cost h3 {
    margin-bottom: 10px;
    text-align: center;
}

.benefit-lead img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.benefit-brand img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.benefit-cost img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}
```
I consolidated all of that into two selectors:
```CSS
.benefit h2 {
    font-size: 20px;
    margin-bottom: 10px;
    text-align: center;
}

.benefit img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}
```


Additionally, there were three different classes for the elements in the main content of the original html, so there were three selectors in the CSS file:
```CSS
.search-engine-optimization {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}

.online-reputation-management {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}

.social-media-marketing {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}
```

All of these classes style the elements the same, so I consolidated all the code into one selector named solution:
```CSS
.solution {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}
```

The same goes for the headers and images inside each solution. Here's what they looked like before:
```CSS
.search-engine-optimization img {
    max-height: 200px;
}

.online-reputation-management img {
    max-height: 200px;
}

.social-media-marketing img {
    max-height: 200px;
}

.search-engine-optimization h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

.online-reputation-management h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

.social-media-marketing h2 {
    margin-bottom: 20px;
    font-size: 36px;
}
```

And after I consolidated everything into two selectors:
```CSS
.solution h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

.solution img { max-height: 200px; }
```

This code is much more elegant and readable!

### CSS Comments
The CSS in any file should be commented to make it easier to understand for those not familiar with the code. It makes it easier to update a website if necessary.
Our code has been thoroughly commented.

## Usage 

Navigate to <a href="https://geminiad.github.io/code-refactor-project">Horiseon Code Refactor</a>

## Credits

Original Website ©Horiseon Social Solution Services, Inc.
Any changes made ©Adam Ferro