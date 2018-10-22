# Styles

## Order of Definitions

The definition blocks should follow the layout of the page's elements: styles for the page's `h1` should (usually) come before styles for the meta.

Media queries can be placed amongst other blocks, but generally should be defined after all other definitions, in descending order of viewport width.

## Order of Properties

When defining a style block, list the properties in the following order (as appropriate):

1. `content`
1. `position`
1. `bottom` or `top`
1. `right` or `left`
1. `z-index`
1. `display`
1. `margin`
1. `padding`
1. `background-image`
1. `background-color`

After that, order properties and their values by character count, so a line with 52 characters would come before a line with 47 characters.

Custom property (variable) assignments should come after all other styles in the definition, since they're inherited by ancestors of the selector.

## Prefixed Properties

If prefixed properties are needed, group and align them for readability:

```css
.foo {
	display: block;
	font-size: 1.2rem;
	
	-webkit-transform: translateX( 5px );
	   -moz-transform: translateX( 5px );
	        transform: translateX( 5px );
}
```

## Nesting

When adding a definition with additional specificity on the previous selector, nest the definition to indicate inheritance:

```css
.foo {
	display: block
}

	// the order may need to change based on the cascade
	.foo:hover {
		color: #fff;
	}

	.foo.bar {
		display: inline-block;
	}
	
		.foo.bar:hover {
			color: #000;
		}
	
.foo::before {
	content: 'bar';
}
```

## Pseudo Elements

Recall that a double colon (`::`) selects a pseudo element, and a single colon (`:`) selects an element's state.

## Text Style Units

The `html` element should specify a base `font-size`, so that `rem` units can be used and easily manage sizes and spacing throughout.

Within text, typically `em` units should be used (except for `font-size`), so those properties are relative to the size of the text.

|Property|Unit|
|:---|:---|
|`font-size`|`rem`|
|`margin`|`em`|
|`padding`|`em`|
|`letter-spacing`|`em`|
|`line-height`|`em`|

There are exceptions of course, but start using the above.

## Spacing

Put in lots of space! Production will use minified code, so use spaces to keep things easily readable:

```css
.foo + .foo {
	margin-top: 5px;
}

.foo:nth-child( 2n + 1 ) {
	width: calc( 50% + 10px );
	background-image: url( https://picsum.photos/200 );
	background-color: rgba( 255, 0, 0, 0.5 );
	transform: translate( 5px, 10px );
}
```