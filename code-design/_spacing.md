# Spacing

A big part of code readability is proper use of line breaks, tabs, and spaces. This document contains guidelines and examples.

## Guidelines

### Use tabs for nesting, spaces for alignment

```
$snafoo = 'bar';
   $foo = 'rab';

if (
	   'bar' === $foo
	|| 'foo' === $foobar
) {
	echo '<p>' .
		'Hello, world!' .
	'</p>';
}

add_action( 'init',    'calyx_frontpage_action__init'    );
add_action( 'wp_head', 'calyx_frontpage_action__wp_head' );
```

### String Concatenation
```php
echo 'Hello, ' . $foo . ' world!';
```

### `if` Conditionals
```php
if ( $foo ) {
	...
}
```

### Function Parameters
```php
function foo( $bar ) {
	...
}

function foo( $bar ) use( $zulu ) {
	...
}
```

### CSS Properties
(also see [_Styles_](styles.md}) document)

In general, add spaces after parentheses and commas, and one empty line break between definitions.

```css
html {
	font-size: 20px;
}

body {
	width: calc( 100% - 50px );
	background-color: rgba( 0, 0, 0, 0.5 );
	transform: translate( -50%, -50% );
}
```

## EditorConfig

> EditorConfig helps maintain consistent coding styles for multiple developers working on the same project across various editors and IDEs. The EditorConfig project consists of a file format for defining coding styles and a collection of text editor plugins that enable editors to read the file format and adhere to defined styles. EditorConfig files are easily readable and they work nicely with version control systems.
([source](https://editorconfig.org/))

Use `.editorconfig` files and supported applications to help ensure standards are followed. The standard `.editorconfig` file will typically look like this:

```
[*]
indent_style = tab
trim_trailing_whitespace = true
```

This config file sets the editor to use tabs for indenting, and to trim trailing whitespace.
