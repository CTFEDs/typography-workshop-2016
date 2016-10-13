autoscale: true,
build-lists: true

# Free fonts

- How free is free?

- Open font license

---

# Free font resources

- [Google Fonts](https://fonts.google.com/)

- [Font Squirrel](https://www.fontsquirrel.com/)

- [The League of Moveable Type](https://www.theleagueofmoveabletype.com/The League of Moveable Type)

- [My Fonts free](https://www.myfonts.com/search/tag%3Afree/fonts/)

---

# `@font-face`

The `@font-face` CSS at-rule allows authors to specify online fonts to display text on their web pages

![](../img/alphabet.jpg)

---

# `@font-face`

The `@font-face CSS` at-rule allows authors to specify online fonts to display text on their web pages

`@font-face` eliminates the need to depend on the limited number of fonts users have installed on their computers.

![](../img/alphabet.jpg)

---

# `@font-face` properties

- `font-family`

- `src`

- `font-weight`

- `font-style`

^
Also `font-variant`, `font-stretch`, `unicode-range`

^
The font-variant property acts as a shorthand for the longhand properties: `font-variant-caps`, `font-variant-numeric`,
`font-variant-alternates`, `font-variant-ligatures`, and `font-variant-east-asian`.

^
The font-stretch property selects a normal, condensed, or expanded face from a font.

^
The `unicode-range` CSS descriptor sets the specific range of characters to be used from a font defined by `@font-face` and made available for use on the current page. If the page doesn't use any character in this range, the font is not downloaded; if it uses at least one, the whole font is downloaded.

![](../img/alphabet.jpg)

---

## `@font-face` example

```
@font-face {
  font-family: 'Open Sans Bold';
  src: url('OpenSans-Bold-webfont.eot');
  src: url('OpenSans-Bold-webfont.eot?#iefix') format('embedded-opentype'),
       url('OpenSans-Bold-webfont.woff2') format('woff2'),
       url('OpenSans-Bold-webfont.woff') format('woff'),
       url('OpenSans-Bold-webfont.ttf') format('truetype'),
       url('OpenSans-Bold-webfont.svg#open_sansbold') format('svg');
  font-weight: normal;
  font-style: normal;
}
```

^ Support all browsers

^ When a font is needed the user agent iterates over the set of references listed, using the first one it can successfully activate.

---

## `@font-face` example

```
@font-face {
  font-family: 'Open Sans Bold';
  src: url('OpenSans-Bold-webfont.eot'); /* IE9 */
  src: url('OpenSans-Bold-webfont.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
       url('OpenSans-Bold-webfont.woff2') format('woff2'), /* Very Modern Browsers */
       url('OpenSans-Bold-webfont.woff') format('woff'), /* Pretty Modern Browsers */
       url('OpenSans-Bold-webfont.ttf') format('truetype'), /* Safari, Android, iOS */
       url('OpenSans-Bold-webfont.svg#open_sansbold') format('svg'); /* Legacy iOS */
  font-weight: normal;
  font-style: normal;
}
```

^ Support all browsers

---

## `@font-face` example additional weight

```
@font-face {
  font-family: 'Open Sans Regular';
  src: url('OpenSans-Regular-webfont.eot');
  src: url('OpenSans-Regular-webfont.eot?#iefix') format('embedded-opentype'),
       url('OpenSans-Regular-webfont.woff2') format('woff2'),
       url('OpenSans-Regular-webfont.woff') format('woff'),
       url('OpenSans-Regular-webfont.ttf') format('truetype'),
       url('OpenSans-Regular-webfont.svg#open_sansregular') format('svg');
  font-weight: normal;
  font-style: normal;
}

```

---

# Styling elements

```
h2 {
  font-family: "Open Sans Bold", Arial, sans-serif;
}
```

---

# Different weight

```
h2 {
  font-family: "Open Sans Regular", Arial, sans-serif;
}
```

---

## Better `@font-face` example

```
@font-face {
  font-family: Open Sans;
  src: local("Open Sans"),
       url(OpenSans-Regular-webfont.woff2),
       url(OpenSans-Regular-webfont.woff);
  font-style: normal;
  font-weight: 400;
}
```

![](../img/alphabet.jpg)

---

## Better `@font-face` example additional weight

```
@font-face {
  font-family: Open Sans;
  src: local("Open Sans Bold"),
       url(OpenSans-Bold-webfont.woff2),
       url(OpenSans-Bold-webfont.woff);
  font-style: normal;
  font-weight: 700;
}
```

![](../img/alphabet.jpg)

---

# Styling elements

```
h2 {
  font-family: "Open Sans", Arial, sans-serif;
  font-weight: 700;
}
```

---

# Different weight

```
h2 {
  font-family: "Open Sans", Arial, sans-serif;
  font-weight: 400;
}
```

---

# Gobal style

body {
  font-family: "Open Sans", Arial, sans-serif;
}

h2 {
  font-weight: 700;
}

---

## Browser support

- woff: all desktop browsers except IE8 and below, Android 4.4+, iOS 5.1+

- woff2: all desktop browsers except IE, Android 5+, iOS 10+

- Opera Mini (mobile browser market share of 44% in SA) does not support `@font-face`

![](../img/alphabet.jpg)