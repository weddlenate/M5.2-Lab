# Accessibility Issues

This is a project that gives us a webpage with a number of accessibility issues that we're tasked with improving. We we're given a few specific things to fix and questions to answer, which are located in the Accessibility Lab Answers at the bottom of this document.

## Getting Started

To get started, clone this repository and run the following commands:

```bash
npm install
```
This will install the necessary dependencies for the project.

## Development

It is recommended to use the VSCode Live Server extension to run the project
locally. This will allow you to see changes in real-time as you make them. There
is no need to run a build process or refresh the page manually. Additionally,
you do not need to setup a local server to run the project.

## Testing

To run the tests for the project, run the following command:

```bash
npm test
```

## Accessibility Lab Answers
Color:
    According to Aim's Color Contrast Checker (https://webaim.org/resources/contrastchecker/), the background and foreground, as is originally given, have a constrast ratio of 4.08:1. This does not meet the 4.5:1 standard. 

    I changed the background to have a hex value of #12D9CC, and now the contrast ratio is 11.82:1.

Semantic HTML:
    1. I'm able to traverse the navigation bar and search bar, but after that I'm immediately taken to the audio file, which skips a lot of the content present on the web page. Also, the navigation bar links and links on the side of the page don't appear to actually link to anything.

    2. Yes, I can make this easier to navigate. I modifications I made were:
        - Changed all <font> elements to <h1>, <h2>, or <h3> elements depending on the desired font size. Changed the corresponding <font> CSS properties to the corresponding header property.
        - Modified text that was separated by <br> elements so they were contained by <p> elements instead. 
        

    3. This should be updated to a <nav> element. I have updated this in the HTML file, as well as the CSS properties that used to target the div element that was there to the new <nav> element

The Images:
    Yes, I have added 'alt' and 'title' attributes to the <img> elements.

The Audio Player:
    1. Yes, I've added a 'Show Transcript' button that allows the user to read the transcript of the audio file when pressed.

    2. I've added a link to the text that shows up when someone is using a browser that doesn't support HTML5 audio players. This link gives them the audio file so they can download it and listen to it that way.

The Forms:
    1. I've added an 'aria-label' attribute to the search bar element that will say "Search through site content" when highlighted by a screen reader.

    2. I've changed the elements surrounding the label text to <label> elements and given them the 'for' attributes so they're associated with their corresponding input elements. 

The Show/Hide Comment Control:
    Yes and yes. I gave the <div> element used as the Show/Hide Comment button the attribute 'tabindex' with a value of '0' so the keyboard is allowed to tab to it. I then added some javascript code that clicks the button whenever it's selected and the 'Enter' key is pressed.

The Table:
    Yes I can. I added the following to the table:
    - Added a caption to the table
    - Gave the titles of each column or row of the table the 'scope="col"' or 'scope="row"' attribute as necessary

Other Considerations:
    1. I changed the very first <div> element to a <header> element
    2. I changed the buttons that activated the search bar and submitted a comment to actual <button> elements instead of <input> elements. 
