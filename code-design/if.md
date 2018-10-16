# `if`

- always use [Yoda conditions](https://en.m.wikipedia.org/wiki/Yoda_conditions): `'foo' === $bar`
- default to using strict comparison (`===`), not loose comparison (`==`)

## Negation
```
if ( !$foo )
	return $bar;
```

## Short
```
if ( 'foo' === $bar )
	return $bar;
```

## Short Two
```
$bar = 'a' === $foo
	? 'aaa'
	: 'bbb';
```

## Short Multiple
```
'a' === $foo && $bar = 'aaa';
'b' === $foo && $bar = 'bbb';
'c' === $foo && $bar = 'ccc';
```

## Long
```
if ( 'bar' === $foo ) {
	$bar = 'foo';
	return $bar . $foo;
}
```

## Simple Inline
`( true === $foo ? 'aaa' : 'bbb' )`

## Complex Inline
```
(
	(
		   true === $foo
		|| true === $bar
	)
	? 'aaa'
	: 'bbb'
)
```