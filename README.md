# regex-pattern

trying to make RegEx patterns easy.

Here are some cases and regular expression patterns solutions.

## Remove time with or without leading zero in a string

**Time format:**

- 09:06 AM
- 9:06 PM
- 9:06
- 19:06

```javascript
const removeTime = txt => {
  if (txt) {
    return date.replace(
      /((0[0-9]|1[0-9]|2[0-3]|[0-9]):[0-5][0-9])|(\s[AaPp][Mm])/g,
      ""
    );
  }
  return txt;
};
```

## Remove html tag element by class, even if it has multiple classes

**html element:**

`<p class="firstClass secondClass">text</p>`

```javascript
const removeElement = txt => {
  if (txt) {
    return txt.replace(/<p class="(.*?)firstClass(.*?)">(.*?)<\/p>/g, "");
  }
  return txt;
};
```
