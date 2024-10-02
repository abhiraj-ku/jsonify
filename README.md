## simple Json parser written in go

json(javascript object notation) has become the de-facto data exchange medium over internet for client and server
This is my attempt to understand how json parsing is done under the hood. This project is inspired by [Build Your Own JSON Parser](https://codingchallenges.fyi/challenges/challenge-json-parser/)

---

## usages

- Parse Simple JSON Object {}
- Step 2: Parse JSON with String Keys and Values
  Goal: Extend the parser to handle string keys and values.
  Lexer: Update to recognize:
  Strings ("key" and "value")
  Colon (:) and comma (,)
  Parser: Validate JSON objects like:

  json

` {"key": "value"}`
Example test cases:
` Valid: {"key": "value"}`
` Invalid: {"key": value}` (missing quotes around value)

Step 3: Parse JSON with Multiple Data Types
`
{
"key1": true,
"key2": null,
"key3": 101
}

`
