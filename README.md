SVG.toDataURL()
===============

The missing SVG.toDataURL() exporter for your SVG elements.

See [original paper][svgopen2010] for more information on interfacing between SVG and Canvas.

Instructions
------------

0. Include [canvg]. Not needed on Firefox 11+!
1. `<script type="text/javascript" src="svg_todataurl.js"></script>`
2. `var pngDataURL = mySVGelement.toDataURL("image/png")`
3. See `butterfly_test.html` for working example.

API documentation
-----------------

See `svg_todataurl.js`.

Compatibility
-------------

Works on all modern browsers. Most browsers require [canvg] for PNG exporting.

Compatibility for May 2012. `+` means "has supported for over 2 years".

	Browser     E x p o r t i n g  f o r m a t
	            svg+xml  png/canvg  png/native
	IE           9+       9+         -
	Chrome       +        +          -
	Safari       +        +          -
	Firefox      +        +          11+ ¹
	Opera        +        +          -

¹ [Allow SVG-as-an-image to be drawn into a canvas without marking it as write-only](https://bugzilla.mozilla.org/show_bug.cgi?id=672013)

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
