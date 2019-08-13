# `do {} while ()`

- always use [Yoda conditions](https://en.m.wikipedia.org/wiki/Yoda_conditions): `'foo' === $bar`
- default to using strict comparison (`===`), not loose comparison (`==`)

## Negation

```
do {
	...
} while ( !$foo );
```

## Short

```
do {
	...
} while ( 'foo' === $bar );
```

## Long

```
do {
	...
} while ( 'bar' === $foo );
```
