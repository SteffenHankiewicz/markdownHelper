# Markdown Helper Utilities
This is a small repository to collect Markdown utitilies to help using Markddown for documentation and protocoll purposes.

## Styling of the Markdown output
To optimise the styling of the Markdown Preview you can find an adapted css-File here. Use it inside of Visual Studio Code by configuring it with one of the following two ways. Please notice that the URL to this css-File has to be used through the jsDelivr CDN as GitHub raw files do contain an unwanded header that VSCode does not accept. Additionally please be careful to use the latest tagged version inside of the URL provided here.

### Configuration user interface
First open the configuration with one of the following ways:

- Click in the Menu `File` → `Preferences` → `Settings` 
- Use the shortcut `⌘` + `,` (Mac) or `Ctrl` + `,` (Windows)

Now select in the configuration dialog on the left `Extensions` → `Markdown` and scroll to `Markdown Styles` to add the following value there:

```
https://cdn.jsdelivr.net/gh/SteffenHankiewicz/markdownHelper@1.5.0/markdown.css
```

### Configuration via settings.json

There are different way to open up the json configuration.
- Open the palette and type `>open user settings` there
- Use the shortcut `⌘` + `,` (Mac) or `Ctrl` + `,` (Windows) and click on the icon in the top right corner (next to the tabs) to switch to json-editor-mode

In this file `settings.json` you can add the following line:

```json
"markdown.styles": [
        "https://cdn.jsdelivr.net/gh/SteffenHankiewicz/markdownHelper@1.5.0/markdown.css"
]
```

## Additional tipps

### Open the configuration of Visual Studio Code always in json-editor-mode
To always open the `settings.json file directly add the following line there:

```json
"workbench.settings.editor": "json",
```
