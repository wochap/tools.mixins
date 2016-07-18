>## This Project Is Deprecated

>Now each mixin has its own module.

# Mixins

The `wocss-tools-mixins` module contains a few framework mixins that are **required** for using any of the rest of wocss.

Install using npm:

```sh
$ npm install --save wocss-tools-mixins
```

## Usage

### [Bem constructor](https://github.com/danielguillan/bem-constructor)

### Breakpoints

Simple media queries mixins.

#### from($size)

Styles take effect from the provided measure and above.

```scss
@include from('lg') { ... }
```

#### to($size)

Styles take effect from zero up to the provided measure.

```scss
@include to('md') { ... }
```

#### from-to($desde, $hasta)

When the screen size is between the two provided measure, the styles in the block will take effect.

```scss
@include from-to(500px, 800px) { ... }
```

### Layout

A few mixins to help tame those layouts.

#### layout-center($max-width, $padding-x)

Center the element.

```scss
.container {
  @include layout-center(1000px, 0);
}
```

#### layout-wrapper()

It makes an element a container as the container [bootstrap](http://getbootstrap.com/css/#overview-container).

```scss
.container {
  @include layout-wrapper();
}
```

#### layout-block()

It makes an element a block.

```scss
.container {
  @include layout-block();
}
```

### Resets

#### reset-input()

Removes any styles that were previously set on a input.

```scss
.form-control {
  @include reset-input();
  // more code
}
```

#### reset-list()

Removes any styles that were previously set on a list, clearing out all the margins and padding that are there by default.

```scss
.items {
  @include reset-list();
  // more code
}
```

#### reset-link()

Removes any styles that were previously set on links, even that annoying text-decoration.

```scss
.article {
  @include reset-link();
  // more code
}
```

## Dependencies

* [wocss-settings-defaults](https://github.com/wocss/settings.default)
