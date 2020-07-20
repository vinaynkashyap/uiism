### How to use breakpoints?

```
  @include media('>=tablet') {
    .foo {
      color: tomato;
    }
  }
```

### How are the responsive classes setup

The responsive classes are setup for the below width size:

    'desktop':   62rem,
    'laptop':   48rem,
    'tablet':   47.9375rem,
    'phablet':   36.25rem,
    'mobile':   30rem

This is a mobile first CSS framework. Meaning any style you apply without a responsive modifier will work on all screen size.

Let's take an example to change the font size in different screen size.

```

<h1 class="font-6x font-md-4x font-sm-3x"> My big heading</h1>


```

The above code translates as below

font-6x is the default font size accross all the screens because it does not have a responsive modifier.
font-md-4x will reuce the font size from 6x to 4x in tablets.
Similar to md font-sm-3x will further reuce the font size from to 3x in mobile phones.

### How to create responsive classes using media queries?

The default responsive classes are setup using the below modifiers.

xl - Desktop
lg - Laptop
md - Tablet
sm - Phablet
xs - Mobile

If you like to create your own version of responsive styles like here is how you do it using the media queries:

font-x { ... }
font-md-x { ... }
font-sm-x { ... }

```

.font-6x {
      color: tomato;
    }

// Tablet styles

  @include media('>=tablet') {
    .font-4x {
      color: tomato;
    }
  }

// Mobile Styles

@include media('>=mobile') {
    .font-3x {
      color: tomato;
    }
  }

```

### Define breakpoints

Define custom breakpoints

```
$breakpoints: (
    'desktop':   62rem,
    'laptop':   48rem,
    'tablet':   47.9375rem,
    'phablet':   36.25rem,
    'mobile':   30rem
) !default;
```
