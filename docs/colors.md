## Adding custom colors and it's usage

<!-- /* // 	Background Colors
// //   -------------------------------------------------------------
// // 	Looping through colors to generate background color with class name .bg-color
// // 	add/delete colors to the array to update background colors
// // 	then use the bg-color class on the html element
// // 	-------------------------------------------------------------
// // 	Example usage & CSS output for background colors
// //
// // 	.grey-100{
// //     background: #d1d1d1;
// // 	}
// // 	<section class="grey-100"> </section>
// //   ------------------------------------------------------------- */ -->

### Add custom colors:

1. Go to `/base/swatches.scss` and define your custom color variables and it's color values.

example:

```
$primary :#f21c1c;
$secondary :#1a1a1a;
$dark :#000;
$light :#cfd8dc;
$success : #00bcd4;
$warning :#fbc02d;
$error :#e53935;

```

### Update config file.

2. A config file in scss project will help you maintain all the variables in one place and serve you as a central control system to make any changes in the future. If you set it up correctly you can update all the variables of your project from this file.

Update the config file from `/base/config.scss` with your new color variables.

```
 $primary : $primary;
 $secondary : $secondary;
 $dark : $dark;
 $light : $light;
 $success :  $success;
 $warning : $warning;
 $error : $error

```

### Update custom backround colors

3. Open `/helpers/bg/bg-colors.scss` file and add the background color variables to the array list.

```
$bg-colors: (

bg-primary $primary
bg-secondary $secondary
bg-dark $dark
bg-light $light
bg-success $success
bg-warning $warning
bg-error $error

);
```

### Color Usage and class reference

We have set up the class names to be same as the material UI color [palette](https://material-ui.com/customization/color/#color-palette)

Background color classes are outputed with the name and numeric value of the color in the material ui palet similar to `.colorname-x` in the output CSS file.

Example of background class:

```
.red-50 { ... }
.red-100 { ... }
.red-200 { ... }
.red-300 { ... }
.red-400 { ... }
.red-500 { ... }
.red-600 { ... }
.red-700 { ... }
.red-800 { ... }
.red-900 { ... }
.red-a100 { ... }
.red-a200 { ... }
.red-a400 { ... }
.red-a700 { ... }

```

The background color is outputed for all color names. It is recommended to remove the background colors which you do not use from the loop to reduce the CSS files size.

Let the fun begin.

To apply the background color to any html element just add the class name.

Example:

```
<div class="red-500">
This div has a red-500 background.
</div>

```
