# `if`

- default to using strict comparison (`===`), not loose comparison (`==`)
- always use [Yoda conditions](https://en.m.wikipedia.org/wiki/Yoda_conditions): `'foo' === $bar`
- it is preferable to "return early" ([read](https://blog.timoxley.com/post/47041269194/avoid-else-return-early)) within a function rather than introducing multiple levels of nesting

The following examples are allowed within code design standards, however, one variation may be easier to read within it's context than another; always consider which is more readable.

## Multiple Conditionals
```php
if (
	   'a' === $foo
	&& 'b' === $bar
	&& 'c' === $zulu
) {
	...
}

// It is usually possible to simplify
// the below statement, but it is permitted.

if (
	(
		   'a' === $foo
		&& 'b' === $bar
	)
	|| 'c' === $zulu
) {
	...
}
```

## Checking for Multiple Values

Instead of doing something like this:

```php
if (
	   1 === $foo
	|| 2 === $foo
) {
	...
}
```

use `in_array()` instead:

```php
if ( in_array( $foo, array( 1, 2 ), true ) ) {
	...
}
```

## Negation Evaluation

```php
if ( !$foo )
	return $bar;
```

## Short Conditional

```php
if ( 'foo' === $bar )
	return $bar;
```

## Short Assignment

```php
$bar = ( 'a' === $foo ? 'aaa' : 'bbb' );
```

## Short, Multiple Conditionals

```php
'a' === $foo && $bar = 'aaa';
'b' === $foo && $bar = 'bbb';
'c' === $foo && $bar = 'ccc';
```

## Long Conditional

```php
if ( 'bar' === $foo ) {
	$bar = 'foo';
	...
	return $bar . $foo;
}
```

## Simple, Inline Conditional

```php
( true === $foo ? 'aaa' : 'bbb' )
```

## Multiple Inline Conditional Statements

```php
(
	(
		   true === $foo
		|| true === $bar
	)
	? 'aaa'
	: 'bbb'
)
```
