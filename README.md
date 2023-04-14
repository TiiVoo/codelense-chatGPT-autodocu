# CodeLens Docu

This is based on the a sample extension that shows the usage of the CodeLens API.

It is not intended as a production quality extension.

- Create a new file
- Write anything
- Click on the CodeLens for action example
- Can be enabled or disabled by command palette

## Demo

![demo](demo.gif)

## VS Code API

### `languages` module

- [`languages.registerCodeLensProvider`](https://code.visualstudio.com/api/references/vscode-api#languages.registerCodeLensProvider)

### CodeLens Provider

- [`CodeLensProvider`](https://code.visualstudio.com/api/references/vscode-api#CodeLensProvider)
- [`CodeLensProvider.provideCodeLenses`](https://code.visualstudio.com/api/references/vscode-api#CodeLensProvider.provideCodeLenses)
- [`CodeLensProvider.resolveCodeLens`](https://code.visualstudio.com/api/references/vscode-api#CodeLensProvider.resolveCodeLens)

## Debugging/Running the Sample via souce:

- Run `npm install` in terminal to install dependencies
- Run `npm install axios` if not installed
- Run `npm install openai`  if not installed
- set chat-GPT key via https://help.openai.com/en/articles/5112595-best-practices-for-api-key-safety
- Run the `Run Extension` target in the Debug View. This will:
	- Start a task `npm: watch` to compile the code
	- Run the extension in a new VS Code window


## Where to start if I want to edit the output and functionality: 
- Edit the documentation output via the function `generateSummary` in `./src/CodelenseProvider.ts` 
- Test via the debugging 
- create PR and discribe change



## To deploy a CodeLens sample and activate it in VS Code, you can follow these general steps:

- Build the CodeLens sample using the command `npm run compile`. This will compile the TypeScript files into JavaScript files and place them in the out folder.
- Copy the entire out folder and paste it into your VS Code extension folder. The extension folder is usually located in C:\Users\<username>\.vscode\extensions on Windows, or ~/.vscode/extensions on macOS and Linux.
- Open the VS Code command palette by pressing Ctrl + Shift + P (Windows, Linux) or Cmd + Shift + P (macOS).
- Type `Extensions: Enable Extension Developer Mode` and select the command from the list. This will enable the developer mode for extensions, which allows you to load your extension without publishing it to the VS Code Marketplace.
- Type `Reload Window` and select the command from the list. This will reload VS Code and activate the changes you made to your extension.
- Open a file in VS Code that your CodeLens sample is supposed to work with. You should see the CodeLens items you defined in your sample code displayed above the text in the editor.