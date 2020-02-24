
## Typography
The typographic settings can be modified using the below variables
### 1. $font-family-base
Define the base font family for the theme. If any external web fonts to be imported, use the @import statement before this varable. The default base font familiy is "`Arial, Helvetica, sans-serif`"

Below SCSS code imports the "Open Sans" font and specifies the base font as 'Open Sans'
```scss
//import font
@import url('https://fonts.googleapis.com/css?family=Open+Sans&display=swap');

// set the base font family
$font-family-base: 'Open Sans';
```
### 2. $font-size-base
The base font size can be assigned to the '$font-size-base' variable as below. Default value is "1 rem"
```scss
$font-size-base: .62 rem;
```
### 3. Heading levels (h1 - h6)
By the heading levels are configured to be relative to the base font size, see the table below. Each of these variables can be overridden

| Levels | Default value |
| -------------- |------------ |
|$h1-font-size    | $font-size-base * 2.5|
|$h2-font-size    | $font-size-base * 2|
|$h3-font-size   | $font-size-base * 1.75|
|$h4-font-size   |$font-size-base * 1.5 |
|$h5-font-size   |$font-size-base * 1.25|
|$h6-font-size   | $font-size-base|

Each of these variables can be modified as per the requirement.
```scss
$h2-font-size : $font-size-base * 1.8;
$h3-font-size : $font-size-base * 1.25;
```
