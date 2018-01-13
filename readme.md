# MultilineStringLiteral

> Multiline String Literals in Java


## Usage

Just call `MultilineStringLiteral.read()` and put a multiline comment between the parentheses. The contents of the comment will be your multiline string

```java
public static String MultilineStringLiteral.read([MultilineStringLiteral.Template... templates])
```

### Basic

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
THIS
IS
$template$
AWESOME
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
