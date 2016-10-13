autoscale: true,
build-lists: true

# Font-display

The font-display descriptor for `@font-face` determines how a font face is displayed based on whether and when it is downloaded and ready to use.

^ Deciding the behavior for a web font as it is loading can be an important performance tuning technique. The new font-display descriptor for @font-face lets developers decide how their web fonts will render (or fallback), depending on how long it takes for them to load.

![](../img/alphabet.jpg)

---

## `font-display` periods

- font block
- font swap
- font failure

![](../img/alphabet.jpg)

^
font-display segments the lifetime of a font download into three major periods.

^
The first period is the font block period. During this period, if the font face is not loaded, any element attempting to use it must instead render with an invisible fallback font face. If the font face successfully loads during the block period, the font face is then used normally.
^
The font swap period occurs immediately after the font block period. During this period, if the font face is not loaded, any element attempting to use it must instead render with a fallback font face. If the font face successfully loads during the swap period, the font face is then used normally.
^
The font failure period occurs immediately after the font swap period. If the font face is not yet loaded when this period starts, it’s marked as a failed load, causing normal font fallback. Otherwise, the font face is used normally.

---

## `font-display` values

- auto
- block
- swap
- fallback
- optional

![](../img/alphabet.jpg)

^
auto uses whatever font display strategy the user-agent uses. Most browsers currently have a default strategy similar to block.

^
block gives the font face a short block period (3s is recommended in most cases) and an infinite swap period. In other words, the browser draws "invisible" text at first if the font is not loaded, but swaps the font face in as soon as it loads. To do this the browser creates an anonymous font face with metrics similar to the selected font but with all glyphs containing no "ink." This value should only be used if rendering text in a particular typeface is required for the page to be useable.

^
swap gives the font face a zero second block period and an infinite swap period. This means the browser draws text immediately with a fallback if the font face isn’t loaded, but swaps the font face in as soon as it loads. Similar to block, this value should only be used when rendering text in a particular font is important for the page, but rendering in any font will still get a correct message across. Logo text is a good candidate for swap since displaying a company’s name using a reasonable fallback will get the message across but you’d eventually use the official typeface.

^
fallback gives the font face an extremely small block period (100ms or less is recommended in most cases) and a short swap period (three seconds is recommended in most cases). In other words, the font face is rendered with a fallback at first if it’s not loaded, but the font is swapped as soon as it loads. However, if too much time passes, the fallback will be used for the rest of the page’s lifetime. fallback is a good candidate for things like body text where you’d like the user to start reading as soon as possible and don’t want to disturb their experience by shifting text around as a new font loads in.

^
optional gives the font face an extremely small block period (100ms or less is recommended in most cases) and a zero second swap period. Similar to fallback, this is a good choice for when the downloading font is more of a “nice to have” but not critical to the experience. The optional value leaves it up to the browser to decide whether to initiate the font download, which it may choose not to do or it may do it as a low priority depending on what it thinks would be best for the user. This can be beneficial in situations where the user is on a weak connection and pulling down a font may not be the best use of resources.

---

# Browser support

![](../img/alphabet.jpg)

---

# none

![](../img/alphabet.jpg)

---

# except

- Behind the _Experimental Web Platform Features_ flag in desktop Chrome 49
- Available in Firefox 46+. To enable, set the 'layout.css.font-display.enabled' pref in about:config to true
- Shipped in Opera and Opera for Android

![](../img/alphabet.jpg)
