# `if`

- default to using strict comparison (`===`), not loose comparison (`==`)
- always use [Yoda conditions](https://en.m.wikipedia.org/wiki/Yoda_conditions): `'foo' === $bar`

## Negation Evaluation
```
if ( !$foo )
	return $bar;
```

## Short Conditional
```
if ( 'foo' === $bar )
	return $bar;
```

## Short Assignment
```
$bar = ( 'a' === $foo ? 'aaa' : 'bbb' );
```

## Short, Multiple Conditionals
```
'a' === $foo && $bar = 'aaa';
'b' === $foo && $bar = 'bbb';
'c' === $foo && $bar = 'ccc';
```

## Long Conditional
```
if ( 'bar' === $foo ) {
	$bar = 'foo';
	return $bar . $foo;
}
```

## Simple, Inline Conditional
`( true === $foo ? 'aaa' : 'bbb' )`

## Complex, Inline Conditional
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