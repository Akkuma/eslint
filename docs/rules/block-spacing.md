# Disallow or enforce spaces inside of single line blocks. (block-spacing)

This rule is for spacing style within single line blocks.

## Rule Details

This rule is aimed to flag usage of spacing inside of blocks.
This rule has a option, its value is `"always"` or `"never"`.

- `"always"` (by default) enforces one or more spaces.
- `"never"` disallows space(s).

### always

```
{
  "block-spacing": [2, "always"]
}
```

The following patterns are considered warnings:

```js
function foo() {return true;}
if (foo) { bar = 0;}
```

The following patterns are not considered warnings:

```js
function foo() { return true; }
if (foo) { bar = 0; }
```

### never

```
{
  "block-spacing": [2, "never"]
}
```

The following patterns are considered warnings:

```js
function foo() { return true; }
if (foo) { bar = 0;}
```

The following patterns are not considered warnings:

```js
function foo() {return true;}
if (foo) {bar = 0;}
```

## When Not to Use It

If you don't want to be notified about spacing style inside of blocks, you can safely disable this rule.
