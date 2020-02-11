# Theming your ace-lib components
## What is an 'ace-lib-theme' theme?
A 'ace-lib-theme' is the set of colors and typography definitions that will be applied on the ace-lib components. Using ace-lib-theme package, you can customize the color and typography of the ace-lib components. 

An ace-lib-theme package contains the core `scss` files which are used to create a theme. These `scss` files needs to be compiled as `css`.

## Using the pre-built sample themes
ace-lib-theme package contains some pre-built theme files. You can use them directly importing into your cui template project. you can use the below options to include.

1. Using css import:
```javascript
@import 'ace-lib-theme/examples/css/blue-green/ace-theme.min.css'
```
2. Directly referencing the file in the html:
```html
<link href="ace-lib-theme/examples/css/blue-green/ace-theme.min.css" rel="stylesheet">
```
## Creating a custom theme
You can create a theme file using the provided SCSS files in `ace-lib-theme` pacakge. The package contains `assets/scss` directory which contians all the Sass files used to build a theme css file. Once the scss files are changed, use the [node-sass](https://www.npmjs.com/package/node-sass) commands to complie them into css. 

Follow the below steps to create an `ace-lib-theme`.

### 1. Install the ace-lib-theme package.

Install the 'ace-lib-theme` from the npm package manager using the below command:

```javascript
npm i ace-lib-theme
```

### 2. Copy the sass files 

Copy the `assets` directory from `node_modules` into the cui templtate's `assets` directory. If you need information about how to create a cui-template, refer to the [cui-template](https://github.com/agileapps-dev-com/agileapps-cui) documentation.

### 3. Make the necessary changes to the `scss` files



### 4. Compile the `scss` files into `css`
Use the below `node-sass` command to compile the scss files into the theme css file :

```javascript
node-sass -c ~path\to\scss\ ~path\to\generated\css\
```
> **Note:** The above command will complile the `ace-theme.scss` file into `ace-theme.css`



