# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Do some research on semantic and non-semantic elements and share your findings. Your response should include:
* Examples of semantic and non-semantic tags
* The differences between semantic and non-semantic tags
* The benefits of using semantic tags (when possible)

### Response 1
Based on the research that I did, my findings were that in HTML, elements can be classified as either semantic or non-semantic each serving a different purpose in terms of readability and accessibility. Here are some examples of semantic tags:

<header>: Which represents the header section of a document or section.
<nav>: Which denotes a navigation section with links to other pages or parts of the document.
<section>: Which represents a distinct section within a document.
<article>: Which is used for standalone, self-contained content, such as a blog post.
<footer>: Which represents the footer for a document or section.
<aside>: Which contains content related to the surrounding content, like side notes or additional info.
<main>: Which specifies the main content of a document.
<figure>: Which is used to associate images, diagrams, and their captions.

Primary examples of non semantic tags look like this:
<div>: Which is a general-purpose block-level container.
<span>: An inline container for text or other inline elements.

Primary differences between semantic and non semantic tags are that sematic tags convey meaning about content structure, improve code readability and understanding for both developers and browsers, enhances accessibility, screen readers and other assistive technologies can interpret them more easily. While non semantic tags act as generic containers and lack inherent meaning, often requiring additional classes or IDs for context. 

One of the benefits of using semantic tags is improved accessibility, semantic elements help assistive technologies interpret and navigate the structure of a webpage. Another benefit of semantic tag is better readability and maintainability: Using elements like <header>, <nav>, or <footer> makes the code more intuitive for developers, reducing the time needed to understand and maintain it.

## Prompt 2

Do some research on accessibility. What are some ways to make your website more accessible? Explain why it is important for developers to create websites that meet accessibility standards.

### Response 2
Using tags like <header>, <main>, <nav>, and <footer> is one way to make your website more accessible, this provides clear structure, making it easier for screen readers and other assistive technologies to understand the layout and purpose of different sections. It is important for developers to create websites that meet accessibility standard becaue accessibility improves usability for everyone, not only those with disabilities. Clear navigation, readable text, and adjustable layouts contribute to a smoother experience for all users.

## Prompt 3

It is possible to add "inline" CSS styles to our html elements using the `style` attribute like so:

```html
<p style="color: red;" >hello world</p>
```

While this is possible, it is a best practice to instead write styles in a separate CSS file. Provide at least one argument for why it _might_ be considered useful to write inline styles, and then provide a more compelling argument for writing styles in a separate CSS file.

### Response 3

An argument for why it would be useful to write inline styles is because inline styles are useful when applying one-off, unique styles to specific elements. For instance, if you need to style a single element differently due to a specific, isolated need, inline styles allow you to quickly make this change without impacting other elements or needing to edit external stylesheets.

An argument for why seperate CSS files on the other hand are useful because seperate CSS files improve reusability and consistency. By defining classes and reusable styles in a CSS file, you can apply consistent styling to multiple elements across different pages, ensuring a compatible look and feel throughout the site.

## Prompt 4

Imagine you are teaching a brand new programmer a brief lesson about the `class` and `id` attributes in HTML as well as how to use them to style elements using CSS. Your lesson should have the following components:

* An explanation of the concept of "classes" and "ids" with an analogy.
* An example of the usage using an HTML code block and a CSS code block.
* An explanation of the syntax using the terms: **attribute**, **selector** 

### Response 4
Think of HTML elements as people at a party. You might want to group some people together, like "friends" or "family," and give them similar characteristics, such as everyone wearing the same color shirt. This is where the class attribute is introduced. A class groups elements together, allowing us to style them the same way. Now, think of a scenario where you need to find one specific person at the party, like the birthday guest. This is where the id attribute is useful. The id is a unique identifier, like a name tag, and it’s used to target one specific element on the page.

<!DOCTYPE html>
<html lang="en">
<head>
  <title>Class and ID Example</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="friend">This is my friend.</div>
  <div class="friend">This is my other friend.</div>
  <div id="birthday-guest">This is the birthday guest!</div>
</body>
</html>

.friend {
  color: black;     
  background-color: white;
  padding: 10px;
}

#birthday-guest {
  color: purple;      
  background-color: lightblue;
  padding: 10px;
}

In HTML, both class and id are attributes you can add to elements. The attribute is additional information about an element, which defines its characteristics. Here, class="friend" and id="birthday-guest" are attributes assigned to <div> elements.

In CSS, selectors target elements in your HTML to apply styles. We use .friend as a class selector in order to style all elements with the class "friend." For the id selector, we use #birthday-guest to style only the element with the id "birthday-guest."


## Prompt 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however is that the best practice?

When building a website, how can I decide which content I should write using HTML/CSS and which content I should create using the JavaScript and the DOM API?

### Response 5

It isn't the best practice to use the DOM API and JavaScript because when it comes to performance  HTML and CSS are optimized for quick processing by the browser, which helps pages load faster compared to JavaScript-generated content. Using DOM API and JavaScript are appropriate for purposes such as interactive elements and dynamic content but using HTML and CSS are more for performance and page structuring and styling. Using HTML/CSS for static content and JavaScript for dynamic content keeps the code modular and maintainable. It also provides a clear separation of concerns, which makes it easier to debug, test, and optimize performance.
