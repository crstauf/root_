# `add_filter`

## Class Method
`add_filter( 'template_include', array( &$this, 'filter__template_include' ) );`

## Global Scope
`add_filter( 'template_include', THEME_PREFIX . '_{$context}_filter__template_include' );`

## Anonymous
```
add_filter( 'template_include', function( $template ) {
	return $template;
} );
```