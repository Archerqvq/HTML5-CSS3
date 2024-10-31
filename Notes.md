- [HTML](#html)
  - [HTML Elements](#html-elements)
  - [\<!DOCTYPE HTML5\>](#doctype-html5)
  - [Attributes](#attributes)
  - [Alt attribute of \<img\>](#alt-attribute-of-img)
  - [Meta elements inside the head with attribute charset](#meta-elements-inside-the-head-with-attribute-charset)
    - [So when a webpage encoding with utf-8 be decoded happens?](#so-when-a-webpage-encoding-with-utf-8-be-decoded-happens)
  - [Hyperlinks](#hyperlinks)
  - [MDN](#mdn)
  - [HTML entity](#html-entity)
  - [Why We Use HTML Entities](#why-we-use-html-entities)
  - [Common HTML Entities Examples](#common-html-entities-examples)
  - [Usage Example](#usage-example)
  - [Semantic HTML](#semantic-html)
  - [Why We Need Semantic HTML](#why-we-need-semantic-html)

## HTML

- HyperText Markup Language
- HTML is a markup language that web developers use to structure and describe the content of a webpage (not a programming language)
- HTML consists of elements that describe different types of content:paragraphs, links, headings, images, video, etc.
- Web browsers understand HTML and render HTML code as websites

### HTML Elements

- Definition: [HTML Elements](https://www.w3schools.com/html/html_elements.asp#:~:text=The%20HTML%20element%20is%20everything,My%20First%20Heading)

### \<!DOCTYPE HTML5>

Every HTML document always needs to start with the so-called DOCTYPE declaration.
And with this let the browser know that we are using HTML in this file.
And all browsers will then know that they should use the HTML5 specification to render this HTML.

### Attributes

Attributes are basically pieces of data, which we can use to describe elements.

### Alt attribute of \<img>

- Allow search engines such as Google Chrome to actually
  know what is in the image because without this description, search engines dont's really have a know of knowing what the image is actually about.
- More important is that by specifying the description of the image, we can also allow blind people to use a website. So users who can use a screen reader will not see the image but instead they will have the screen reader read the alternative text to them **(This is the meaning of technology)**.

### Meta elements inside the head with attribute charset

Adding `charset="UTF-8"` to a webpage tells the browser to interpret the page’s content as UTF-8, a character encoding that can represent any character in the Unicode standard. This is especially important for displaying text accurately across multiple languages and symbols, ensuring that characters like accented letters, non-Latin scripts, emojis, and symbols display correctly.

Without specifying UTF-8, the browser may default to a different encoding, potentially causing characters to render incorrectly, especially if the page includes special symbols or multilingual text. By including `<meta charset="UTF-8">` in the `<head>` of your HTML document, you ensure a consistent character interpretation for users across different regions and browsers.

#### So when a webpage encoding with utf-8 be decoded happens?

The decoding step happens as soon as the browser receives and begins interpreting the HTML file. Here’s how it works:

1. **Receiving the HTML Content**: When the browser requests an HTML page, it receives raw bytes of data from the server.

2. **Reading the Charset**: Early in the HTML file, if `<meta charset="UTF-8">` is present (usually within the `<head>` tag), the browser reads this instruction and knows to decode the incoming bytes as UTF-8. This needs to happen as soon as possible so that it can decode all following characters correctly.

3. **Decoding the Bytes to Characters**: Based on the UTF-8 setting, the browser interprets each sequence of bytes and maps them to characters as defined by the UTF-8 encoding standard.

4. **Rendering the Text**: Once decoded, the characters are assembled and rendered as text on the webpage.

If the charset isn’t defined, the browser may guess the encoding, but this can lead to garbled text if it guesses incorrectly. Specifying UTF-8 ensures that the interpretation process happens predictably and accurately.

### Hyperlinks

One of the fundamental building blocks of the internet are hyperlinks or for short just links.
So links are what actaully enables the internet to be a worldwide web.

### MDN

MDN, short for **Mozilla Developer Network**, is an open-source platform providing comprehensive documentation and resources for web technologies, including HTML, CSS, JavaScript, and more. Created and maintained by Mozilla, MDN is widely regarded as one of the most reliable and accessible references for both new and experienced web developers.

Some of the resources you’ll find on MDN include:

- **Documentation** for core web languages and APIs, such as HTML, CSS, JavaScript, and DOM manipulation.
- **Interactive examples and code snippets** to help visualize concepts and test code directly in the browser.
- **Tutorials and guides** on web development topics, covering everything from basic syntax to advanced programming practices.
- **Browser compatibility tables** for each language or feature, detailing how different web browsers support them.

MDN is regularly updated by contributors, ensuring that it reflects the latest standards and best practices in web development.

### HTML entity

HTML **entities** are special codes that represent reserved characters (like `<`, `>`, `&`) or characters not easily typed on a keyboard (like `©`, `®`, and non-ASCII characters). They start with `&` and end with `;`, and when used, they are displayed as their respective symbols or characters on a webpage.

### Why We Use HTML Entities

Some characters, such as `<` and `>`, have special meanings in HTML (they're used for tags). If you want to display these characters as text rather than part of the HTML structure, you need to use entities. For example:

- `<` should be written as `&lt;`
- `>` should be written as `&gt;`
- `&` should be written as `&amp;`

### Common HTML Entities Examples

- **Special characters**:
  - `<` = `&lt;`
  - `>` = `&gt;`
  - `&` = `&amp;`
- **Non-keyboard characters**:
  - `©` = `&copy;`
  - `®` = `&reg;`
  - `€` = `&euro;`
- **Spacing characters**:
  - ` ` (non-breaking space) = `&nbsp;`

### Usage Example

```html
<p>
  Use &lt; and &gt; to write HTML tags in plain text without them being
  rendered.
</p>
<p>&copy; 2024 OpenAI</p>
```

Entities ensure your HTML content is displayed as you intend, even if it includes characters with special meanings.

### Semantic HTML

**Semantic HTML** refers to using HTML tags that convey the meaning and structure of the content on a webpage rather than just how it looks. Semantic elements like `<header>`, `<footer>`, `<article>`, `<section>`, `<nav>`, and `<main>` define the purpose of the content they enclose.

### Why We Need Semantic HTML

1. **Improves Accessibility**: Screen readers and other assistive technologies rely on semantic HTML to interpret content correctly, making websites more accessible for visually impaired users.
2. **Enhances SEO**: Search engines use semantic HTML to understand the structure and context of content on a page, which can improve a site’s search rankings.

3. **Better Code Readability and Maintainability**: Semantic HTML provides structure, making code easier to read, understand, and maintain for developers.

4. **Consistent Styling**: It enables consistent styling and layout by applying styles to specific elements (e.g., `<header>` or `<nav>`), rather than using classes or IDs alone.

Using semantic HTML aligns the structure of a page with its meaning, creating a clearer hierarchy that benefits both humans and machines interacting with the content.
