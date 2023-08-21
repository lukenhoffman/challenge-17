# Regex Tutorial: The Deep Dive into the `$` Symbol

Welcome, dear reader, to an in-depth exploration of the `$` symbol in regular expressions. As a significant component of regex, understanding the intricacies of `$` is vital for mastering pattern matching.

## Summary
The `$` symbol serves as an end anchor in regex. Its primary purpose is to assert a position at the end of a line or string, making it invaluable for patterns that need to validate the tail-end of input data.

## Table of Contents
1. [The Fundamentals of `$`](#dollar-basics)
2. [Multiline Mode and `$`](#multiline)
3. [Using `$` with Other Quantifiers](#quantifiers)
4. [Common Mistakes with `$`](#mistakes)
5. [About the Author](#author)

---

### <a name="dollar-basics"></a>1. The Fundamentals of `$`

In regex, the `$` doesn't match a character; it matches a position. Specifically:

- `$`: Asserts position at the end of a line or string.

It can be used in conjunction with other regex components to ensure a certain sequence of characters is found at the end.

**Example:**  
Regex: `world$`  
Matches: "Hello world" but not "world peace"

---

### <a name="multiline"></a>2. Multiline Mode and `$`

The behavior of `$` can vary based on regex flags. Specifically, in multiline mode (often represented with the `m` flag), `$` can match the end of any line within a multiline string, not just the very end of the entire string.

**Example:**  
Regex: `end.$` in multiline mode  
Matches:  
- The `end.` in "This is the end.\nBut not the end of everything."

Without the `m` flag, `$` would only match the end of the entire string.

---

### <a name="quantifiers"></a>3. Using `$` with Other Quantifiers

In combination with quantifiers, the `$` symbol can be used to match patterns of varying lengths at the end of a string.

**Examples:**  
- Regex: `\d$` - Matches strings ending with a single digit.
- Regex: `\d{3}$` - Matches strings ending with three digits, like "123".
- Regex: `colou?r$` - Matches strings ending in "color" or "colour".

---

### <a name="mistakes"></a>4. Common Mistakes with `$`

1. **Not accounting for whitespace:**  
   If the input string has trailing whitespace, a regex pattern ending with `$` might not match as expected. To account for potential trailing whitespace, you can use `\s*$` which matches any amount of whitespace at the end.

2. **Forgetting about multiline mode:**  
   Without the multiline flag, `$` only matches the end of the entire string, which can lead to unexpected results in multiline inputs.

3. **Misplacing `$`:**  
   Ensure `$` is at the very end of your regex pattern (or right before a global flag). Placing it elsewhere can lead to unexpected matching behaviors.

---

### <a name="author"></a>4. About the Author

This tutorial was created by [Luken Hoffman](https://github.com/lukenhoffman). Luken is a newcomer to the software devolpment field and hopes to simplify andd demistify the world of coding for other newcomers like himself.

---

As you continue your regex adventure, keep in mind the versatility and power of the $ symbol. Through careful application and understanding, you'll be able to harness its capabilities to the fullest. Happy coding!