# Stylus @font-face mixin
A Stylus mixin to manage font import with the @font-face property.

### Dependencies
  * [stylus](https://github.com/LearnBoost/stylus)

Example:
```stylus
@import "fontFace"

fontFace("../font/", lato-regular, "Lato")
fontFace("../font/", menlo-regular, "Menlo", 700, regular, woff2)
```

Will output:
```css
@font-face {
  font-family: "Lato";
  src: url("../font/lato-regular.eot");
  src: url("../font/lato-regular.woff2") format("woff2"), url("../font/lato-regular.woff") format("woff"), url("../font/lato-regular.ttf") format("truetype");
  font-weight: 400;
  font-style: normal;
}
@font-face {
  font-family: "Menlo";
  src: url("../font/menlo-regular.woff2") format("woff2");
  font-weight: 700;
  font-style: normal;
}
```
Complete list of arguments:

- fontP: Path to fonts folder *required
- fileN: Files name without extension *required
- fontF: font-family *required
- fontW: font-weight
- fontS: font-style
- formats: font formats woff2 woff truetype eot

Support with all format enabled (default):

Chrome 3.5+, Safari 3+, Firefox 3.5+, Opera 10.1+, IE 7+ (eot support IE9 Compat Modes), Android 2.2+, iOs 4.3+

## Credits

Developed by [Alexis Gaillard](https://alexisgaillard.com/). Licensed under [MIT](http://opensource.org/licenses/mit-license.php).
