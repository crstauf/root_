# `while`

- always use [Yoda conditions](https://en.m.wikipedia.org/wiki/Yoda_conditions): `'foo' === $bar`
- default to using strict comparison (`===`), not loose comparison (`==`)

## Negation
```
while ( !$foo )
	$foo--;
```

## Short
```
while ( 'foo' === $bar )
	$foo++;
```

## Long
```
while ( 'bar' === $foo ) {
	$bar = 'foo';
	$foo = $bar . $foo;
}
```