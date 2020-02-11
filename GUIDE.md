# Theming your ace-lib components
## What is an 'ace-lib-theme'?
A 'ace-lib-theme' is the set of colors and typography definitions that will be applied on the ace-lib components. Using ace-lib-theme package, you can customize the color and typography of the ace-lib components. 

An ace-lib-theme package contains the core `scss` files which are used to create a theme. These `scss` files needs to be compiled as `css`.


## Creating a custom theme
You can create a theme file using the provided SCSS files in `ace-lib-theme` pacakge. The package contains `assets/scss` directory which contians all the Sass files used to build a theme css file. Once the scss files are changed, use the [node-sass](https://www.npmjs.com/package/node-sass) commands to complie them into css. 

Follow the below steps to create an `ace-lib-theme`.

### 1. Install the ace-lib-theme package.

Install the 'ace-lib-theme` from the npm package manager using the below command:

```javascript
npm i ace-lib-theme
```

### 2. Copy the sass files 

Copy the `scss` directory from `node_modules/ace-lib-theme/assets/` into the cui template's `assets/themes/` directory. If you need information about how to create a cui-template, refer to the [cui-template](https://github.com/agileapps-dev-com/agileapps-cui) documentation.

### 3. Make the necessary changes to the `scss` files

Make changes to the scss files as required and then compile the scss files into `ace-theme.css`. [Understand the structure of the scss files](#understanding-the-structure-of-ace-lib-theme-theme) from below.

>**Important Note:** It's highly recommended to retain the scss files and directory structure as it is. Use `_add-on-styles.scss` for your custom additional css style definitions.



### 4. Compile the `scss` files into `css`
Use the below `node-sass` command to compile the scss files into the theme css file :

```javascript
node-sass -c ~path\to\scss -o ~path\to\generated\css\
```
> **Note:** The above command will complile the `ace-theme.scss` file into `ace-theme.css`

### 5. Use the `ace-theme.css` into the template's `index.html`
The generated css theme file should be linked to the template html file.

```html
<link href="~path/to/generated/css/ace-theme.css" rel="stylesheet">
```

## Understanding the structure of `ace-lib-theme` theme
The root directory of scss file contains the below important files:

```scss
\---scss
    |   ace-theme.scss
    |   _add-on-styles.scss
    |   _colors.scss
    |   _typography.scss
    |   
    +---components
    |   |   
    |   +---ace-elements
    |   |           
    |   +---common               
    \---utilities
```

| File/Directory | Description |
| -------------- |------------ |
| ace-theme.scss    | The main scss file. It imports all other internal scss files. |
| _add-on-styles.scss    | The scss file which contains the your addtional customizations. Any additional css definitions or customizations are to be part of this file. |
| _colors.scss   | The color palettes definitions for the theme. Change the color values in this scss file. This scss file should not contain any other specifications other than color palettes and color variables. |
| _typography.scss    | The scss file to specify the typography for the theme. It should not contain any other definitions other than typography definitions. |
| components/ace-elements  | Directory contains the ace-lib element specific style definitions. |
| components/common  | directory contains the internal components used inside ace-lib elements, such as checkbox, radiobutton, table, tab,etc. |

## Using the pre-built sample themes
`ace-lib-theme` package contains some pre-built sample theme files. You can use them directly importing into your cui template project. You can use the below options to include. 

>**Note:** You will need to update the path to `node_modules` directory in the below reference code.

1. Using css import:
```javascript
@import 'node_modules/ace-lib-theme/examples/css/blue-green/ace-theme.min.css' ;
```
2. Directly referencing the file in the html:
```html
<link href="node_modules/ace-lib-theme/examples/css/blue-green/ace-theme.min.css" rel="stylesheet">
```