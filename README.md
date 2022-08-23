# Markdown Helper Utilities
This is a small repository to collect Markdown utitilies to help using Markddown for documentation and protocol purposes.

## Styling of the Markdown output
To optimise the styling of the Markdown Preview you can find an adapted css-File here. Please notice that the URL to this css-File has to be used through the jsDelivr CDN as GitHub raw files do contain an unwanded header that Visual Studio Code does not accept. Additionally please be careful to use the latest tagged version inside of the URL provided here.

To use the provided css-styling open up the configuration file `settings.json` of Visual Studio Code like written below  and add the following line:

```json
"markdown.styles": [
        "https://cdn.jsdelivr.net/gh/SteffenHankiewicz/markdownHelper@1.5.0/markdown.css"
]
```

## Styling of the Markdown editor highligting
To change the way how the editor is doing the highlighting of the source code do the following:
- open up the configuration file `settings.json` of Visual Studio Code like written below
- paste the following snippet into the configuration file:

```json
"editor.tokenColorCustomizations": {
        "[Default Light+]": {
            "textMateRules": [
                {
                    "scope": "markup.italic.markdown",
                    "settings": {
                        "foreground": "#c7254e",
                        "fontStyle": "bold"
                    }
                },{
                    "scope": "heading.3.markdown",
                    "settings": {
                        "foreground": "#418be4",
                        
                    }
                }
            ]
        }
    }
```


- use the palette to open up `>Inspect Editor Tokens and Scopes` to find out the element you like to style differntly


## Additional tipps

### Open the configuration file `settings.json` of Visual Studio Code in json-editor-mode
There are different way to open up the json configuration.
- Open the palette and type `>open user settings` there
- Use the shortcut `⌘` + `,` (Mac) or `Ctrl` + `,` (Windows) and click on the icon in the top right corner (next to the tabs) to switch to json-editor-mode


### Always open the configuration of Visual Studio Code always in json-editor-mode
To always open the `settings.json` file directly with the shortcut add the following line in that file:

```json
"workbench.settings.editor": "json",
```
