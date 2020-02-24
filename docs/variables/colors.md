
## Colors
Below are the important color variables:
### 1. $theme-colors
It is a color [map](https://sass-lang.com/documentation/values/maps). For every color mentioned in this map, corresponding [utility css color classes]() will be generated.

The default map contains the below color Map:
```scss
$theme-colors: (
    "primary": #6200ee,
    "secondary": #03dac6,
    "error": #b00020,
    "light": #f8f9fa,
    "dark": #343a40
  );
``` 
Though, the default `$theme-colors` variable contains only 5 colors, more number of 'named' maps can be added. See the example below:

```scss
$theme-colors: (
    "primary": #6200ee,
    "secondary": #03dac6,
    "error": #b00020,
    "light": #f8f9fa,
    "dark": #343a40,
    "blue-gray":#607D8B,
    "blue-color":#03A9F4,
    "purple":#9C27B0
  );
```

The `$theme-colors` map values can be accessed like below:
```scss
map-get($theme-colors, "purple");
```
#### Utility color classes for $theme-colors map:
For every color map present in the $theme-colors map, separate color utility classes will be generated.
There are 2 types of color utility classes availble
1. Background colors: The background color utility classes are prefixed with `ace-bg-`. This can be used to style any elements in the page.
    ```html
        <div class="ace-bg-primary">.ace-bg-primary</div>
    ```
2. Text colors: The text color utility classes are prefixed with `ace-text-`. 
    ```html
        <p class="ace-text-primary">.ace-text-primary</p>
    ```
