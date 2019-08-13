# `while`

- always use [Yoda conditions](https://en.m.wikipedia.org/wiki/Yoda_conditions): `'foo' === $bar`
- default to using strict comparison (`===`), not loose comparison (`==`)

## Negation

```php
while ( !$foo )
	$foo--;
```

## Short

```php
while ( 'foo' === $bar )
	$foo++;
```

## Long

```php
while ( 'bar' === $foo ) {
	$bar = 'foo';
	$foo = $bar . $foo;
}
```
