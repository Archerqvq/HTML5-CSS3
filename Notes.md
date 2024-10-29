- [HTML](#html)
  - [HTML Elements](#html-elements)
  - [\<!DOCTYPE HTML5\>](#doctype-html5)
  - [Attributes](#attributes)
  - [Alt attribute of \<img\>](#alt-attribute-of-img)
  - [Meta elements inside the head with attribute charset](#meta-elements-inside-the-head-with-attribute-charset)
    - [So when a webpage encoding with utf-8 be decoded happens?](#so-when-a-webpage-encoding-with-utf-8-be-decoded-happens)

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
  knwo what is in the image because without this description, search engines dont's really have a know of knowing what the image is actually about.
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
