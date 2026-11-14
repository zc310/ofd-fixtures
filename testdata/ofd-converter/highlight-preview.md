# Code highlighting

## Go

```go
package main

// Print a greeting.
func main() {
    name := "world"
    println("Hello, " + name, 42)
}
```

## JavaScript

```js
const greet = (name) => {
    // Template string
    return `Hello, ${name}!`;
};
console.log(greet("world"));
```

## Plain code (no language)

```
func main() {
    println("No language: gray text", 42)
}
```

> [!TIP]
> Highlighted code also works inside alerts:
>
> ```python
> def add(a, b):
>     # Keep the original spacing.
>     return a + b
> print(add(10, 20))
> ```
