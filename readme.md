# MultilineStringLiteral

> Multiline String Literals in Java


## Usage

Just call `MultilineStringLiteral.read()` and put a multiline comment between the parentheses. The contents of the comment will be your multiline string

```java
public static String MultilineStringLiteral.read([MultilineStringLiteral.Template... templates])
```

Depending on your project structure, you might need to update `MultilineStringLiteral.directory`

*This is obviously not meant for use in production code, but I found it quite useful for use in unit tests*

### Multiline Strings

```java
String text = MultilineStringLiteral.read(
/*
some
multiline
string
*/
);
```

Equivalent to:
```java
String text = "some\nmultiline\nstring";
```

### Template Substitution

You can pass one or more `MultilineStringLiteral.Template` objects to the `read` function to replace placeholders w/ custom content:

```java
String text = MultilineStringLiteral.read(
        new MultilineStringLiteral.Template("$template$", "really")
/*
this
is
$template$
awesome
*/
);
```

Result:
```
this
is
really
awesome
```

## License
MIT @ [Lukas Kollmer](https://lukaskollmer.me)
