# `add_action`

## Class Method
`add_action( 'init', array( &$this, 'action__init' ) );`

## Global Scope
`add_action( 'init', THEME_PREFIX . '_{$context}_action__init' );`

## Anonymous
```
add_action( 'init', function() {
	...
} );
```