# Article Progression - Parts 1-4

## Part 1 - Basic HTML Elements

You task for this assignment is to use your knowledge of basic HTML elements to build a web page for an article. Feel free to use whatever topic you want for your article.

In general, you want to start off with an rough design/schematic for your page before you start. A **wireframe** is the term used for the mockup created to visualize the initial rendering of the page. A wireframe is a rough visual representation of the page. Here is the wireframe for the page you are going to create for this assignment.

![](https://raw.githubusercontent.com/hoc-labs/images/main/article-1.png)

### Create index.html

Create your new HTML page in your project folder. Name it index.html. Once you have generated your boiler-plate HTML, don't forget to change the &lt;title&gt; element to something more meaningful for your page.

### Lorem Ipsum Text

A technique front-end developers use when they need some text to display in prototypes (non-production code), is to use sample text supplied by sites like [https://loremipsum.io/](https://loremipsum.io/).


You can specify whether you want paragraphs or sentences, and it will generate some sample text that you can then copy and use in your pages.

Not only does it prevent you from having to come up with your own narrative, but it also keeps the people reviewing your web page from getting distracted by the text, and instead focus on the overall design review.

In this assignment, there are several places where you will need to use some Lorem Ipsum text.

### Title Section

This is the title for your entire page. Use an `h1` element.

For the author byline, use an `<p>` element.

### Video Section

You can add a video to your page using the &lt;video&gt; element. There are several attributes necessary to include the various controls on the video. The attributes for adding controls to the the video are: autoplay, muted, and loop. They are boolean attributes. Just placing the attribute on the element (with no associated value) is all that is needed to activate the functionality. For example, here is now those attributes would be specified.

```markup
<video src="" controls autoplay muted loop />
```

| Attribute | Purpose |
| :--- | :--- |
| src | The value of the src attribute can be a path to a local image or an URL to a remote video. |
| controls | whether the control panel is visible. |
| autoplay | whether it starts automatically |
| muted | whether the audio is muted by default |
| loop | whether the video plays in a loop |

Look on [pexels.com](http://www.pexels.com) for free videos on your topic. Enter "videos [topic]" in the search box, then right click on a video to bring up the context menu and click the "Copy video address" option. You will use that URL for the **src** attribute of the `<video>` element.

After the video, insert some Lorem Ipsum text to describe the video.

### Article TOC (Table of Contents)

Before the three sections, there is a heading, followed by a list of three items. They are links to the sections further down the page. Clicking on the link will scroll down to that section of the page. Use an `<h2>` element for this heading. To create the list, use `<ul>`/`<li>` elements with an `<a>` element inside each `<li>` element to create the links to each of the sections.

### Internal Page Links

Most of the time the value of the href attribute on the `<a> ` element is the URL for an external page with in the website, or a page within another website (usually launches a new tab for this type).

But it is also possible to set the href attribute to the id of another element in the same page. Click on this type of hyper-link will cause the target element to scroll into view. This is particularly useful for very long articles where there is an index to sections at the top and clicking on a link in the index scrolls the page down to the appropriate section.

For our article we are going to use this technique to link the items in the TOC list to their associated sections further down in the article.

In order to do this, you will need to give each section heading (the `<h3>` element) an id attribute with a unique value. Then, in the `<a>` element linking to the section heading, you will specify that **\#id** as the value for the href attribute.

For example, here is how we could create a hyper-link to the section heading further down the page.

```markup
<a href="#section1">Section 1</a>

<!-- more stuff here -->

<h3 id="section1">Section1</h3>
```

## Article Detail Sections

There are going to be three different sections in the article, each detailing something about your topic.

For each section, there will be:

* a heading - use an `<h3>` element
* followed by a paragraph of text - use a `<p>` element
* followed by an image about the topic - use an `<img>` element
* and finally, a caption under the image (byline for the image author) - use a `<p>` element.

Inside the paragraph of text for one of your topic sections, embed a hyper-link to an external page about your topic. For example, if your topic is soccer, you could link to your favorite site about soccer. Remember to use the **target** attribute on the `<a>` element with a value of "\_blank" to make the new page come up in a separate window.

Just like you did for your video, you can use the [pexels.com](http://www.pexels.com) or [unsplash.com](http://www.unsplash.com) websites to get access to free images to use in your web page. Again, just right click on the image, and choose the "Copy image address" option to copy the URL for the image. Use that URL as the value for the src attribute on the `img` element.

## Sample Completed Article

Here is what a sample article with the topic of jelly fish looks like. Only the first topic section is included in the screen capture. There would be two more sections following the Pink Jelly section: one for the Orange Jelly and one for the Yellow Jelly. Clicking on the links in the Meet the Jellies TOC would cause the page to scroll down and bring the corresponding into view.

![](https://raw.githubusercontent.com/hoc-labs/images/main/article-2.png)

Remember to get in the habit of using **git ACP** (add, commit, push) to save snapshots of your work whenever you feel you have reached a new milestone and would like to preserve your progress.

When you are done, do it one last time to make sure your final work is on GitHub for your instructor to review.

<br/><br/>

## Part 2 - Semantic HTML Elements
You task for this assignment is to improve your topic article to use semantic elements. 

## Section Element

The first step is to use the `<section>` element to wrap sections of the HTML element tree that are logically grouped together so that you can use that to later style each section. In the screen capture below, each of these elements should be wrapped in a `<section>` element. I have left out the last two topic sections. They would follow the same pattern as Section 1.

![](https://raw.githubusercontent.com/hoc-labs/images/main/article-sections.png)

Here is an example, of wrapping the elements for Section 1, which is for the Pink Jelly section in my example.

```markup
<!--------------------- Pink Jelly ---------------------->
<section>
  <h3 id="pink-jelly">Pink Jelly</h3>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing
  elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Egestas tellus rutrum tellus
  Tellus rutrum tellus pellentesque eu tincidunt tortor aliquam nulla facilisi. Libero justo laoreet sit amet cursus sit.
  </p>
  <p>Vel quam elementum pulvinar etiam non quam lacus suspendisse. Tincidunt dui ut ornare lectus sit amet
      est placerat in. Lectus nulla at volutpat diam ut  venenatis tellus.
  </p>
  <p> Sally Smith</p>
</section>
```

You should the following areas of your HTML wrapped in  `<section>` elements:

* Article Title Section
* Video Section
* Article TOC Section
* Each Article Topic Section

## Title Section

Use the `<address>` element to display the author's name instead of the `<p>` element.

[address docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/address)

## Article Detail Sections

Use the &lt;figure&gt; element to wrap both the image and the caption below the image.

[figure/figurecaption docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure)

## Top-level Layout Elements

Inside the `<body>` element, wrap all of the content with an `<article>` element, to indicate that the content is an article.

Then, wrap the portion labelled header below with a `<header>` element and the portion labelled main with a `<main>` element.

![](https://raw.githubusercontent.com/hoc-labs/images/main/semantic-sections.png)

[main docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main)

That's it. You now have a document ready for for the next step: applying some CSS.

Use the **git ACP** (add, commit, push) commands to update GitHub with your work.

<br/><br/>
## Part 3 - Basic CSS

You task for this assignment is to improve your topic article in two ways:
* add more detail to the Article Title Section
* add a CSS stylesheet and style the content

### Article Title Section

* Add a sub-title under the article title. Use a `<p>` element, with some lorem ipsum text. Place the sub-title immediately following the article title `<h1>`.
* Add a profile image for the author. Add an `<img>` element following the sub-title. Use the photo.jpg image in the images folder.
* Add a `<time>JANUARY/FEBRUARY 2018</time>` element following the `<address>` element.

It should look something like this after the elements have been added.

![](https://raw.githubusercontent.com/hoc-labs/images/main/article-progression-article-title-changes.PNG)


### Create a Stylesheet

* Create a CSS stylesheet file named styles.css in your project folder.
* Include styles.css in your index.html file using the `<link rel="stylesheet" href="styles.css">`.
  
  <br/>
### Styles - Overall Document
**Adding some space around the content**

Add some padding between the edge of the page and the content.

**Change the default font to "Poppins"**

[Using Google Fonts](https://chnn-anne.gitbook.io/html-css/basic-css/google-fonts)

Once you have changed the default font, you should be able to verify the change because the Poppins font does not have the serif typography.

**Change the default font size to 18px**
<br/>
**Add topic section spacing**
Add some space between each of the jellyfish topic sections. You should use margins for space between element boxes and padding for space within an element's box.

<br/>
###Styles - Article Title Section
Here's a screen capture of what the title section should look like.

![](https://raw.githubusercontent.com/hoc-labs/images/main/article-progression-title.png)
 

**Author Profile Photo**
* Make the image round (hint: search for border-radius, round)
* Set the width and height to a size that fits well on the line.

**Article Title Section Fonts**
* Change the article title `<h1>` font to 32px
* Change the article sub-title font-size to 24px.

**Adjust Margin between Title and Sub-title elements**
Before styling, there is too much space between the title (`<h1>`) and the sub-title (`<p>`). Because both have a default margin, and margins collapse, setting one to zero will not remove the space. You will need to set both the bottom margin of the title and the top margin of the sub-title to zero to completely remove the margin, and the play with values for one or the other to get the desired space.

**Style - Author Section**
We want to get the author's profile image, name, and article date all to show up on a single line and also adjust the text color and font weight.

* the address element is a block element by default. change it to be inline so that it does not return to the next line.
* set the text color for the address to be a shade of red.
* set the font size to be 11px for both the address and the time elements
* set the font weight to be 600 for both the address and the time elements
* adjust the avatar styles to make it center vertically (vertical-align:middle) and add a margin on the right of 5px.

### Styles - Article TOC
Here's a screen capture of what we want it to look like.
  
![](https://raw.githubusercontent.com/hoc-labs/images/main/meet-the-jellies.png)

* change the color of the links to the the same shade of red as in the author section.
* add a bottom border the heading
* add a bottom border to the list of links

## Part 4 - Article Comments
Add a comments section to the bottom of the article.
* use flex to position the buttons
* use flex to position the avatar to the left of the comment details for each user.


![](https://raw.githubusercontent.com/hoc-labs/images/main/article-progression-part4.png)

