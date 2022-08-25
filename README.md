# Markdown Helper Utilities
This is a small repository to collect Markdown utitilies to help using Markddown for documentation and protocol purposes.

## tl;dr
### Copy all configuration and Styling
- Open the palette and type `> Open user settings` (either directly in json mode or toggle to json view by using the icon on the top right)
- Select all and replace it with the content of the file [settings.json](VisualStudioCode/settings.json) there

### Copy user snippets
- Open the palette and type `> Snippets: Configure User Snippets` and select 'Markdown' afterwards
- Select all and replace it with the content of the file [markdown.json](VisualStudioCode/markdown.json) there


<br/>
<hr/>

## Detailed explaination

### Styling of the Markdown output
To optimise the styling of the Markdown Preview you can find an adapted css-File here. Please notice that the URL to this css-File has to be used through the jsDelivr CDN as GitHub raw files do contain an unwanded header that Visual Studio Code does not accept. Additionally please be careful to use the latest tagged version inside of the URL provided here.

To use the provided css-styling open up the configuration file `settings.json` of Visual Studio Code [like written below](#open-the-configuration-file-of-visual-studio-code-in-json-editor-mode) and add the following line:

```json
"markdown.styles": [
        "https://cdn.jsdelivr.net/gh/SteffenHankiewicz/markdownHelper@1.7.0/VisualStudioCode/markdown.css"
]
```

### Customised highlighting inside of the Markdown editor 
To change the way how the editor is doing the highlighting of the source code do the following:
- open up the configuration file `settings.json` of Visual Studio Code [like written below](#open-the-configuration-file-of-visual-studio-code-in-json-editor-mode)
- make sure your theme is in the list of supported themes inside of the snippet, otherwise adapt the snippet
- copy the [part from the element `editor.tokenColorCustomizations`](VisualStudioCode/settings.json#L15-L50) and paste it into your `settings.json` file

### Configure User Snippets
To allow user specific snippets do the following:
- Open the palette and type `> Snippets: Configure User Snippets`
- Select `markdown.json (Markdown)`
- Paste the [content from this repository 'markdown.json'](VisualStudioCode/markdown.json) there


### Additional tipps

#### Open the configuration file of Visual Studio Code in json-editor-mode
There are different way to open up the json configuration file `settings.json`:
- Open the palette and type `> Open user settings` 
- Use the shortcut `⌘` + `,` (Mac) or `Ctrl` + `,` (Windows) and click on the icon in the top right corner (next to the tabs) to switch to json-editor-mode


#### Always open the configuration of Visual Studio Code always in json-editor-mode
To always open the `settings.json` file directly with the shortcut add the following line in that file:

```json
"workbench.settings.editor": "json",
```

#### Find out the elements inside of editor for customised styling
For an individual styling of markdown source elements you can use the palette to switch on an inspector that shows how the class names are labeled. To open this inspector do the following:

- use the palette to open up `> Inspect Editor Tokens and Scopes` 
- hover over the elements you want to inspect
- get the name from `textmate scopes` inside of the inspector

You can see this in action here: https://egghead.io/lessons/vs-code-adding-custom-syntax-highlighting-to-a-theme-in-vscode
