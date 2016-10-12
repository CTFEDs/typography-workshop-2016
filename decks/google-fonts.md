## Google Fonts

The Google fonts API allows us to add open source web fonts to a website. Adding stylish fonts to your site has never been easier!

---

### How do I take advantage of this AMAZING Google offer?

- Simply visit [Google Fonts](https://fonts.google.com/)

- Browse through the fonts in the directory and click the + icon to add a typeface to your selection

---

![inline](../img/google-fonts-1.PNG)

---

### Once you are done browsing, open the arbitrarily positioned "selection drawer" lurking at the bottom of the screen...

---

![inline](../img/google-fonts-2.PNG)

---

### You can still customize your selection in this view by choosing or excluding font variants in the "customize" tab

---

![inline](../img/google-fonts-3.PNG)

---

### Google kindly indicates the load time that the selected fonts will incur. Note the load time "fast" in an appealing shade of green

---

### Google will generate all the code you need to include the font.

---

### Copy and paste the following line of code in the `<head>` of your document:

---

```
<link href="https://fonts.googleapis.com/css?family=Open+Sans" rel="stylesheet">
```

---

![inline](../img/google-fonts-4.PNG)

---

### Finally, specify the following rule somewhere in your CSS and you're good to go! For example:

___

```
body {
  font-family: 'Open Sans', sans-serif;
}
```

---

### SUPER DUPER EASY HUH?

---

### What about multiple fonts?

---

### No problem, Google's got ya covered!

---

### You can select multiple typefaces and include them all in just one line of code!

---

```
<link href="https://fonts.googleapis.com/css?family=
Open+Sans:300,300i,400,400i,600,600i,700,700i,800,800i"
rel="stylesheet">
```

---

### However, that handy load time hint in the "selection drawer" will tell you all those fonts will be "slow", in a bright, warning red!

---

### There are only three speed indicators, "fast", "moderate" and "slow". A bit of an oversight really, because that many fonts will actually be "insufferably slow".

###

---

### Google fonts, so easy they're dangerous...

---

### It's so easy to include them, many developers add them with abandon and don't realise the cost.

---

### Too many linked Google fonts will impact performance as your site waits for fonts to load from the Google API.

---

### Extra fonts mean extra bytes to download, and in South Africa, data ain't cheap!

___

### Most importantly though, in the event of flaky internet connection, you'll treat your users to a lovely blank page while it waits for those external resources to download.

---

### Hmmm, easy yes, but with consequences.
