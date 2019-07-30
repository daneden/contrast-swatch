> Adapted from [jxnblk/contrast-swatch](https://github.com/jxnblk/contrast-swatch)

[![][hero]][hero]

[hero]: https://contrast-swatch.daneden.now.sh/cff/40f?size=256

# Contrast Swatch

Image microservice for color contrast information

[![][a]][a]
[![][b]][b]
[![][c]][c]

[a]: https://contrast-swatch.daneden.now.sh/bcf/409
[b]: https://contrast-swatch.daneden.now.sh/98f/206
[c]: https://contrast-swatch.daneden.now.sh/fff/40f

## Usage

Contrast swatch images can be used in any place an image is rendered.
The URL accepts a foreground and background color.

[`https://contrast-swatch.daneden.now.sh/cff/40f`][example]

[example]: https://contrast-swatch.daneden.now.sh/cff/40f

**HTML**

```html
<img src="https://contrast-swatch.daneden.now.sh/fff/07c" alt="color contrast indicator" />
```

**Markdown**

```md
![color contrast indicator](https://contrast-swatch.daneden.now.sh/fff/07c)
```

## React

You can wrap the image in a React component (or any templating engine) for generating documentation.

```js
import React from 'react'

export default ({
  foreground,
  background,
  ...props
}) =>
  <img
    {...props}
    src={`https://contrast-swatch.daneden.now.sh/${foreground}/${background}`}
    alt='color contrast indicator'
  />
```

## Customization

Use URL queries to customize the styles.

```
https://contrast-swatch.daneden.now.sh/fff/40f?width=256&height=96&fontSize=1.25
```

**Pass/Fail Label**

[![][pass]][pass]
[![][fail]][fail]

[pass]: https://contrast-swatch.daneden.now.sh/cff/40f?width=256&height=128&label=1
[fail]: https://contrast-swatch.daneden.now.sh/a6f/40f?width=256&height=128&label=1

**Font Size**

[![][smallfont]][smallfont]
[![][largefont]][largefont]

[smallfont]: https://contrast-swatch.daneden.now.sh/cff/40f?width=256&height=128&fontSize=0.5
[largefont]: https://contrast-swatch.daneden.now.sh/cff/40f?width=256&height=128&fontSize=2

**Size**

[![][large]][large]
[![][small]][small]

[large]: https://contrast-swatch.daneden.now.sh/cff/40f?size=320
[small]: https://contrast-swatch.daneden.now.sh/cff/40f?size=48

**Width & Height**

[![][wide]][wide]
[![][tall]][tall]

[wide]: https://contrast-swatch.daneden.now.sh/cff/40f?width=256&height=48
[tall]: https://contrast-swatch.daneden.now.sh/cff/40f?width=32&height=48

**Custom Text**

[![][text]][text]

[text]: https://contrast-swatch.daneden.now.sh/cff/40f?width=256&text=Aa

**Font Weight**

[![][weight]][weight]

[weight]: https://contrast-swatch.daneden.now.sh/cff/40f?fontWeight=900&width=256

**Radius**

[![][rounded]][rounded]
[![][circle]][circle]

[rounded]: https://contrast-swatch.daneden.now.sh/cff/40f?radius=8
[circle]: https://contrast-swatch.daneden.now.sh/cff/40f?radius=48

**rgb**

Compare two `rgb` values, or an `rgb` and a hex value:

```
https://contrast-swatch.daneden.now.sh/rgb(255,255,255)/40f?width=256&height=96&fontSize=1.25
```

[![][rgb]][rgb]

[rgb]: https://contrast-swatch.daneden.now.sh/rgb(255,255,255)/40f?width=256&height=96&fontSize=1.25


## Options


Option | Description
---|---
`size`      | Width & height in pixels
`width`     | Width of image in pixels
`height`    | Height of image in pixels (font size will scale based on height)
`fontSize`  | Relative font size (default 1)
`fontWeight`| Font weight (default 1)
`label`     | Show a pass/fail label based on the [WCAG Criteria][wcag]
`radius`    | Border radius
`baseline`   | Shift text baseline down
`text`      | Render any custom text

## Metadata

A JSON response with color contrast information can be fetched by adding the `type=json` query to the URL.

```
https://contrast-swatch.daneden.now.sh/cff/40f?type=json
```

**Note:** the returned JSON schema might change in a future version

[wcag]: https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-contrast.html

## Related

- [Colorable](https://colorable.jxnblk.com)
- [Use Contrast](https://usecontrast.com/)

MIT License
