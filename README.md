SVG.toDataURL()
===============

The missing `SVG.toDataURL()` for your SVG elements. Supports exporting as SVG+XML and PNG.

See [original paper][svgopen2010] for more information on interfacing between SVG and Canvas.

Instructions
------------

1. Include [canvg] if you need PNG support for unsupported browers (see compatibility below).
2. `<script type="text/javascript" src="svg_todataurl.js"></script>`
3. See `butterfly_test.html` for full example & compability test.

```javascript
mySVGelement.toDataURL("image/png", {
    callback: function(data) {
        myIMGelement.setAttribute("src", data)
    }
})
```

API documentation inside [svg_todataurl.js](svg_todataurl.js).

Compatibility
-------------

Test your browser with our [butterfly test suite](http://sampumon.github.io/SVG.toDataURL/butterfly_test.html).

Works in all modern browsers. Some browsers require [canvg] for PNG exporting.

Compatibility as of October 2017. `+` yes, `vv+` yes since version vv, `-` no support yet.

	Browser     E x p o r t i n g  f o r m a t
	            SVG+XML  PNG/canvg  PNG/native
	IE           9+       9+         edge
	Chrome       +        +          33+ ²
	Safari       +        +          7.1+ ³
	Firefox      +        +          11+ ¹
	Opera        +        +          +

¹ [Allow SVG-as-an-image to be drawn into a canvas without marking it as write-only](https://bugzilla.mozilla.org/show_bug.cgi?id=672013)  
² [Implement SVGImage::hasSingleSecurityOrigin()](https://bugs.webkit.org/show_bug.cgi?id=119492)
³ [Test Browser Support for SVG to Canvas](http://designashirt.github.io/svg-canvas-tests/)

Notes
-----

* SVG `<image>` elements only work if their `src` is a dataURL. External images, same domain or not, will not be rendered (but won't cause a security exception either).

Final
-----

Licensed with the permissive MIT license, as follows.

Copyright (c) 2010,2012 Sampu-mon & Mat-san

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

[canvg]:http://code.google.com/p/canvg/
[svgopen2010]:http://svgopen.org/2010/papers/62-From_SVG_to_Canvas_and_Back/
