
<!-- Projeect off on -->
<img src="https://i.ibb.co/4tKP5fY/eslint-setup.png" width="100%">

<!-- PROJECT Title -->
<br />
<p align="center">
  <h3 align="center"><a href="https://github.com/suncodebd/EslintSetup/">React and Next.js Eslint and Prettier setup for auto code Formating and Best practice</a></h3>

<!-- TABLE OF CONTENTS -->



## Table of Contents


- [Editor Setup](#editor-setup)
  - [Plugins](#plugins)
  - [Settings](#settings)
  - [Set Line Breaks](#set-line-breaks)
- [Linting Setup](#linting-setup)
  - [Install Dev Dependencies](#install-dev-dependencies)
  - [Create Linting Configuration file manually](#create-linting-configuration-file-manually)
- [Contact](#contact)

<!-- HOW TO RUN -->

Please follow the below instructions to run this project on your computer:


<!-- Editor Setup -->

## Editor Setup

You can use any editor but I personally prefer VS Code. I will give some instructions about how I prefer VS code to be set up for React and next.js applications.

### Plugins

You need to install the below plugins:

- ESLint by Dirk Baeumer
- Prettier - Code formatter by Prettier


### Settings

Follow the below settings for VS Code -

1. Create a new folder called ".vscode" inside the project root folder
2. Create a new file called "settings.json" inside that folder.
3. Paste the below json in the newly created settings.json file and save the file.

```json

 // .vscode/settings.json
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.fixAll.tslint": true,
    "source.organizeImports": true
  },
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.formatOnSave": false
  },
  "[typescript]": {
    "editor.formatOnSave": false
  },
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact"
  ],
  // emmet
  "emmet.triggerExpansionOnTab": true,
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "typescript": "typescriptreact"
  },
  "typescript.tsdk": "node_modules/typescript/lib"
}



```

If you followed all previous steps, the theme should change and your editor should be ready.

### Set Line Breaks

Make sure in your VS Code Editor, "LF" is selected as line feed instead of CRLF (Carriage return and line feed). To do that, just click LF/CRLF in the bottom right corner of editor, click it and change it to "LF". If you dont do that, you will get errors in my setup.

<img src="https://i.postimg.cc/tgp8WD4h/Screenshot-2022-06-04-222059.png" alt="Line Feed" width="100%">

## Linting Setup

In order to lint and format your React project automatically according to popular airbnb style guide, I recommend you to follow the instructions below.

### Install Dev Dependencies one by one 

```sh
# ESLint and TypeScript
npm install --save-dev eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin

# Prettier
npm install --save-dev prettier eslint-config-prettier eslint-plugin-prettier

```

or You can also add a new script in the scripts section like below to install everything with a single command:


### Create Linting Configuration file manually

Create a `.eslintrc.js` file in the project root and enter the below contents:

```sh

// .eslintrc.js
module.exports = {
  parser: '@typescript-eslint/parser',
  extends: [
    'plugin:@typescript-eslint/recommended',
    'plugin:prettier/recommended',
  ],
  plugins: ['@typescript-eslint', 'prettier'],
  rules: {
    'prettier/prettier': 'error',
  },
};


```
Create a .prettierrc file for Prettier configuration:

```json 

// .prettierrc
{
  "semi": true,
  "singleQuote": false,
  "jsxSingleQuote": false,
  "tsxSingleQuote": false,
  "trailingComma": "all",
  "printWidth": 80,
  "tabWidth": 2,
  "endOfLine": "auto"
}


```

<!-- CONTACT -->

## Contact

Md Minarul islam - [devctme@gmail.com](mailto:devctme@gmail.com)

Youtube Setup Video Link: [Eslint setup](https://youtu.be/Krg3lCbBuds](https://youtu.be/P9ti7ma5e_s)

Youtube Channel: [DevCT]( https://www.youtube.com/channel/UC0B-8Ks4pmRigOs-UsORkbQ)

