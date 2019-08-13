# `if`

- default to using strict comparison (`===`), not loose comparison (`==`)
- always use [Yoda conditions](https://en.m.wikipedia.org/wiki/Yoda_conditions): `'foo' === $bar`

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
	return $bar . $foo;
}
```

## Simple, Inline Conditional

```php
( true === $foo ? 'aaa' : 'bbb' )
```

## Complex, Inline Conditional

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
