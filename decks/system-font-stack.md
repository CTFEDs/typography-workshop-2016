# system<br>font<br>stack

![](../img/alphabet.jpg)

---

```css
body {
  font-family: -apple-system,
  sans-serif;
}
```

^ something like this
we'll come back to it

---

## Which font<br>loads the fastest?

![](../img/alphabet.jpg)

---

## The font that doesn't need a network request

![](../img/alphabet.jpg)

---

## Vendors becoming more focused on typography

![](../img/alphabet.jpg)

---

## Google: Roboto
## Apple: San Francisco
## Microsoft: Segoe UI

![](../img/alphabet.jpg)

^ Droid Sans

---

### Big sites doing it

## Medium
## Wordpress
## Ghost
## Github

![](../img/alphabet.jpg)

---

### Two ways to do it

## 1. Magic shorthand
## 2. Family list

![](../img/alphabet.jpg)

---

# 1. Magic shorthand

---

# `font: menu;`

![](../img/alphabet.jpg)

^ couple of other keywords

---

## borks on iOS
## borks for many<br>on Android
## shorthand prop,<br>so "heavy"

^ font size, weight
cannot be combined
no fall back

![](../img/alphabet.jpg)

---

# 2. Family list

![](../img/alphabet.jpg)

---

```css
body {
  font-family: Helvetica, Arial, sans-serif;
}
```

^ familiar
stack
talk it through

![](../img/alphabet.jpg)

---

```css
body {
  font-family: -apple-system,
  BlinkMacSystemFont,
  "Segoe UI",
  Roboto,
  Oxygen-Sans,
  Ubuntu,
  Cantarell,
  "Helvetica Neue",
  sans-serif;
}
```

![](../img/alphabet.jpg)

^ OS X and iOS Safari. BlinkMacSystemFont: Chrome on Mac OS X.
Windows and Windows Phone
Android
Linux flavours
fallbacks


---

# :thumbsdown:?

^ Like device sniffing
Need to keep it up to date (how often?)
Won't cover them all
Might load "the wrong one"?

![](../img/alphabet.jpg)
