# markdown-it-shiki-twoslash

## 2.0.19

### Patch Changes

- Updated dependencies [86d6214]
  - remark-shiki-twoslash@3.0.5

## 2.0.18

### Patch Changes

- Updated dependencies [e5ecfea]
  - remark-shiki-twoslash@3.0.4

## 2.0.17

### Patch Changes

- Updated dependencies [bc5330b]
  - remark-shiki-twoslash@3.0.3

## 2.0.16

### Patch Changes

- Updated dependencies [56b4e11]
  - remark-shiki-twoslash@3.0.2

## 2.0.14

### Patch Changes

- Updated dependencies [8fffcd9]
  - remark-shiki-twoslash@3.0.0

## 2.0.2

### Patch Changes

- Updated dependencies [bbba24f]
  - remark-shiki-twoslash@2.0.5

## 2.0.1

### Patch Changes

- remark-shiki-twoslash@2.0.4

## 2.0.0

### Major Changes

- 372ef26: Remove extra trailing newline in code blocks before twoslash processing

### Patch Changes

- 61a6af5: Adds support for an annotation system. This is still work in progress, but the goal is to allow you to provide a way to write meta-commentary on a code-sample from the outside of the code block by having an arrow and some comments.

  For example

  ````
  ```js twoslash
  function compact(arr) {
  // @annotate: left 56 - No editor warnings in JavaScript files<br/><br/>This crashes at runtime.
    if (orr.length > 10) return arr
    return arr
  }
  ```
  ````

  Would create a codeblocck with:

  ```js
  function compact(arr) {
    if (orr.length > 10) return arr;
    return arr;
  }
  ```

  And a little SVG arrow and the text "No editor warnings in JavaScript files<br/><br/>This crashes at runtime." next to it.
  I'll be tweaking the syntax over time, but for now the syntax is `// @annotate: [left/right] [arrow degree rotatation] [text degree rotatation] - Text to show`

- Updated dependencies [61a6af5]
  - remark-shiki-twoslash@2.0.3

## 1.1.12

### Patch Changes

- remark-shiki-twoslash@2.0.1

## 1.1.11

### Patch Changes

- 8a0fcc0: Switch to use a new package which we've extracted out from Shiki Twoslash for handling parsing the different potential formats for codefence attributes: [fenceparser](https://www.npmjs.com/package/fenceparser) which means a breaking change in the remark plugin API. The semver major shouldn't affect anyone using the library via another tool (e.g. via the docusaurus plugins etc).
- Updated dependencies [8a0fcc0]
  - remark-shiki-twoslash@2.0.0

## 1.1.9

### Patch Changes

- Updated dependencies [f92d030]
  - remark-shiki-twoslash@1.5.6

## 1.1.8

### Patch Changes

- remark-shiki-twoslash@1.5.5
