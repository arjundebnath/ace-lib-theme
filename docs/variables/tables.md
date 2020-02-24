## Tables
Below table variables are avilable for customizing.

### Variables

| Variable | Default value | Description |
| -------------- |------------ |------------ |
| $table-cell-padding    | 0.25rem | Tabel cell padding. |
| $table-select-cell-width | 0 | Select column width. This is applicable only on the column with checkboxes. |
| $table-color | $body-color | The text color inside the table. |
| $table-bg| null | Background color for the table.|
|$table-accent-bg| rgba($black, 0.05) | background color for the stripped rows. Applicable only on `.ace-table-striped` applied table.|
|$table-hover-color| $table-color | Text color for the hovered row. Applicable only for `.ace-table-hover` applied tables. |
|$table-hover-bg| rgba($black, 0.075) |Background color for the stripped rows. Applicable only for `.ace-table-hover` applied tables. |
|$table-border-width| $border-width | Border width for the table cells. Applicable only for `.ace-table-bordered` applied table. |
|$table-border-color| $border-color | Border color for the table. Applicable only for `.ace-table-bordered` applied table.   |
|$table-head-bg| $gray-200 | Table header background color |
|$table-head-color| $gray-700 | Table header text color |
|$table-striped-order| odd | The row order selector config for `.ace-table-striped` applied table |

Each of the above variable can be assigned with different values as below:
```scss
$table-head-bg : map-get($theme-colors, "purple"); // This map color must be present in the $theme-colors map.

$table-border-width: 2px;
```
### Table utility classes

| classes |  Description |
| -------------- |------------ |
| .ace-table-bordered    | Adds borders all around the table and between all the columns. |
| .ace-table-borderless    | Removes borders all around the table and between all the columns. |
| .ace-table-striped    | Applies Zebra-striping effect. |
| .ace-table-hover   | Placed here since it has to come after the potential zebra striping. |