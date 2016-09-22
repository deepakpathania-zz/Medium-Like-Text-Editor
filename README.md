# Medium-Like-Text-Editor
- A medium like text editor with functionality like paragraph division, customizable toolbar with bold, italic, anchor and colouring functionality. 
- Based on medium-editor library.
- Replaces all four letter words with a random word on clicking replace. (Test feature, change it if you feel like)
- More than 15 customizable options in the toolbar window, check out the medium-editor library for reference.

# Quick Start
- Clone this repository on your local machine.
- cd to this repository and enter <code>npm install --save</code> in the terminal to install and save all dependencies.
- Open the index.html file to edit the main editor area. 
```html
    <div id="container">
        <h1>Start editing..</h1>
        <div class="editable" id="test" ondrop="drop(event)" ondragover="allowDrop(event)"> <!--This is the main editing area where the paragraphs get populated when one hits enter -->
        </div>
    </div>
  ```
- Change styling and stuff by overriding the css by making a <code>custom.css</code> file or edit the <code>css/demo.css</code> file.
- Change the editor and add more options to the toolbar by altering the following code snippet as per your need.
```javascript
        var editor = new MediumEditor('.editable', { //creates a new editor object
            toolbar: { //used to specify buttons in the toolbar, has more than 15 options including text justification, headings and blockquote options.
                buttons: ['bold', 'italic', 'underline', 'highlighter', 'anchor']
            },
            buttonLabels: 'fontawesome',
            autoLink: true,
            paste: {
            forcePlainText: false,
            },
            extensions: {
            'highlighter': new HighlighterButton()
                }
            }),
        cssLink = document.getElementById('medium-editor-theme');
```

# Demo Screenshots
- After succesfully following the steps, you should be good to go and see the following image on opening <code>index.html</code> in any of your browser.

![selection_035](https://cloud.githubusercontent.com/assets/15071438/18762655/56308068-8127-11e6-92ec-652ca4fd23ca.png)

- As you start typing and hit enter, a new paragraph is created. So each enter press creates a new paragraph.

![selection_036](https://cloud.githubusercontent.com/assets/15071438/18762656/56328e9e-8127-11e6-97fa-edc3b8c17f42.png)

- Highlight any text region by either selecting through dragging mouse or use shift to select and a toolbar should appear above it with options like Bold, Italics, Underline, Highlight and Anchor.

![selection_037](https://cloud.githubusercontent.com/assets/15071438/18762654/562fa86e-8127-11e6-90cd-919f654009c5.png)


![selection_038](https://cloud.githubusercontent.com/assets/15071438/18762657/56373f98-8127-11e6-9c96-3b0606f76a26.png)


![selection_039](https://cloud.githubusercontent.com/assets/15071438/18762659/5653c460-8127-11e6-9176-7ee6e6361f46.png)

- Type any four letter word and click replace, it takes the entire text, splits it, check for length and replace it with a four letter random word by sending an ajax request to a random word generating API. Just for testing purposes, feel free to do whatever with this feature.

![selection_040](https://cloud.githubusercontent.com/assets/15071438/18762658/563ff37c-8127-11e6-9d7f-78fcca562df8.png)


![selection_041](https://cloud.githubusercontent.com/assets/15071438/18762660/56e7a1e4-8127-11e6-932e-13bcececc35c.png)

