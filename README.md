<h1 align="center">
  <br>
  Hori<span color="#d9dcd6">seo<span>n
  <br>
</h1>

<h3 align="center">A website providing solutions to help your business grow</h3>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#accessibility-changes">How To Use</a> •
  <a href="#download">Download</a> •
  <a href="#credits">Credits</a> •
  <a href="#related">Related</a> •
  <a href="#license">License</a>
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
HTML should provide the structure of a webpage and CSS should provide the styling. Reducing the amount of styling in the html document should make it easier to read. The following changes were made to reduce the styling in html:

-

### Accessible Alt Attributes
Screen readers read the output of a website. It's important alt attributes are defined so that screen readers will properly read an image and disabled folks can enjoy any website. The following changes were made to make images more accessible:

### Heading Attributes in Sequential Order
There should only be 1 h1 header, the next header should be an h2, and one shouldn't use h3 unless it's a subheader of an h2. It's good practice. The following changes were made to facilitate that:

### Concise, Descriptive Title
Each website should have a short, descriptive title so that people know where they are navigating to.

### Links All Function Correctly
All the links in a website should work.

### CSS Consolidation
The amount of code should be a minimum in any project/website in order to reduce reduncancy and make values easy to read/change. A minimum amount of code makes our code easy to read and modify.

### CSS Comments
The CSS in any file should be commented to make it easier to understand for those not familiar with the code. It makes it easier to update our website if necessary.

## Usage 

Provide instructions and examples for use. Include screenshots as needed. 

To add a screenshot, create an `assets/images` folder in your repository and upload your screenshot to it. Then, using the relative filepath, add it to your README using the following syntax:

```md
![alt text](assets/images/screenshot.png)
```


## Credits

List your collaborators, if any, with links to their GitHub profiles.

If you used any third-party assets that require attribution, list the creators with links to their primary web presence in this section.

If you followed tutorials, include links to those here as well.


## License

The last section of a good README is a license. This lets other developers know what they can and cannot do with your project. If you need help choosing a license, use [https://choosealicense.com/](https://choosealicense.com/)


---

🏆 The sections listed above are the minimum for a good README, but your project will ultimately determine the content of this document. You might also want to consider adding the following sections.

## Badges

![badmath](https://img.shields.io/github/languages/top/nielsenjared/badmath)

Badges aren't _necessary_, per se, but they demonstrate street cred. Badges let other developers know that you know what you're doing. Check out the badges hosted by [shields.io](https://shields.io/). You may not understand what they all represent now, but you will in time.

## Features

If your project has a lot of features, consider adding a heading called "Features" and listing them there.

## Contributing

If you created an application or package and would like other developers to contribute it, you will want to add guidelines for how to do so. The [Contributor Covenant](https://www.contributor-covenant.org/) is an industry standard, but you can always write your own.

## Tests

Go the extra mile and write tests for your application. Then provide examples on how to run them.