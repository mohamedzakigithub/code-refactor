# Code Refacor

## Description

The aim of this project is to refactor the company home page code ( HTML/CSS) to follow the Web Content Accessibility Guidelines (WCAG).

[Click here to the view Page](https://mohamedzakigithub.github.io/code-refactor/)

## Table of Contents

- [What is WCAG](#What%20is%20WCAG)
- [Implementation](#Implementation)
- [References](#References)

## What is WCAG

WCAG is a single shared standard for web content accessibility that meets the needs of individuals, organizations, and governments internationally. The goal of this standard is to make web content more accessible to people with disabilities or socio-economic restrictions.

## WCAG Implementation and code refactor

The web page in this repository was edited to follow the WCAG standars and code readability as follows.

### Add page title

A title was added to the page \<title> element with the company name.

<title>
  Horiseon Social Solution Services, Inc. SEO & More.
</title>

### Use of semantic HTML tags

All non-semantic HTML tags in the document were replaced by HTML5 semantic tags to make the document follow a logical structure independent of styling and positioning. This was done by replacing \<div> tags by \<header>, \<section>, \<article>, \<aside> and \<footer>.

Example

```
<!-- Header section including nav bar-->
<header class="header">
  <h1>Hori<span class="seo">seo</span>n</h1>
  <!-- Nav bar section inculding navigation links-->
  <nav>
    <ul>
      <li>
        <a href="#search-engine-optimization">Search Engine Optimization</a>
      </li>
      <li>
        <a href="#online-reputation-management">Online Reputation Management</a>
      </li>
      <li>
        <a href="#social-media-marketing">Social Media Marketing</a>
      </li>
    </ul>
  </nav>
</header>
```

### Use of Alt attributes in all images

Alt attribute was added to all images in the page with a description of the picture displayed. this will help users with restricted vision or blind to know what is displayed when using screenreader software. A picture were added using the "content" property in CSS as a background, this pictures were changed and now uses the \<img> tag to enable the use of Alt attribute on it.

Example

```
<img class="main-image" src="assets/images/digital-marketing-meeting.jpg" alt="Digital Marketing Meeting" />
```

### Use of code comments

Code comments were added throughout the code before each logical section to help in code readability and future reference.

Example

```
<!-- Footer section containing copyright notice -->
<footer>
  <h2>Made with ❤️️ by Horiseon</h2>
  <p>
    &copy; 2019 Horiseon Social Solution Services, Inc.
  </p>
</footer>
```

### Fixed broken link

A link in the navigation bar was fixed as the target \<div> was missing the id.

Broken code

```
<div class="search-engine-optimization">
  <img src="./assets/images/search-engine-optimization.jpg" class="float-left" />
  <h2>Search Engine Optimization</h2>
  <p>
    The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
  </p>
</div>

```

Fixed code

```
<article id="search-engine-optimization" class="search-engine-optimization">
  <img src="./assets/images/search-engine-optimization.jpg" class="float-left" alt="Search Engine Optimization" />
  <h2>Search Engine Optimization</h2>
  <p>
    The dominance of mobile internet use means that users are searching for the right business as they travel,
    shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility
    and find the right customers for your business.
  </p>
</article>
```

## References

- [Web Accessibility Initiative Home page](https://www.w3.org/WAI/)
- [Easy Checks – A First Review of Web Accessibility](https://www.w3.org/WAI/test-evaluate/preliminary/#title)
- [HTML5 Semantic Elements](https://www.w3schools.com/html/html5_semantic_elements.asp)
