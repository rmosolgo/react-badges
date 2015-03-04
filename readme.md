## Badge

I thought it would be fun to make badges that were like github badges, but said whatever I wanted :) So I grabbed the SVG version from ... gemnasium, I think, then went to work.

You can [try it on github pages](http://rmosolgo.github.io/react-badges/)!

The interesting parts are:

- you can go from SVG to PNG in browser:
  - Make a data URI from the SVG ([src](https://github.com/rmosolgo/react-badges/blob/master/index.html#L40))
  - Make an image tag with that data URI for a `src` ([src](https://github.com/rmosolgo/react-badges/blob/master/index.html#L40-L43))
  - After the image loads, write it to a canvas ([src](https://github.com/rmosolgo/react-badges/blob/master/index.html#L48-L49))
  - Then get a new data URI (for a PNG) from the canvas ([src](https://github.com/rmosolgo/react-badges/blob/master/index.html#L50))
- you have to escape SVG before making into a data URI ([src](https://github.com/rmosolgo/react-badges/blob/master/index.html#L8))
- some parts of SVG weren't supported by React, so I had to sub them in manually ([src](https://github.com/rmosolgo/react-badges/blob/master/index.html#L37-L39))
- the SVG is actually hidden -- it's just used as a reference to generate the PNG ([src](https://github.com/rmosolgo/react-badges/blob/gh-pages/index.html#L76-L81))
