# monte-carlo-pi
A visual Javascript implementation of the Monte Carlo method being used to calculate Pi.

For more information on how this came to be written, see https://danq.me/2015/06/14/calculating-pi/.

## Usage

Open monte-carlo-pi.html in a modern web browser (definitely NOT IE8).
Requires support for inline SVG, and benefits from a fast Javascript
interpreter. Modify the file itself to tweak the options.

## Methodology

An inefficient but easily-understandable way to estimate the value of pi using
a computer is to use a Monte Carlo experiment. To understand this, consider the
following: take a square piece of grid paper with both axes labelled from
-1 to 1, and draw a circle of radius 1 with its centre at the centre of the paper.
That circle is described by the formula x<sup>2</sup> + y<sup>2</sup> = 1.
Choose any point on that graph paper, and call it (x,y): now we know that if
for this point x<sup>2</sup> + y<sup>2</sup> is *less than* 1, then it must lie
*inside* the circle (this is logical, because it must lie on the circumference
of a circle with a smaller radius but the same centre as our original circle).
Similarly, any point for which x<sup>2</sup> + y<sup>2</sup> is *greater* than
1 must lie *outside* the circle.

The ratio of the area inside a circle relative to the area outside a circle but
inside the smallest square that encloses that circle is pi/4. Therefore, if we
choose points at random within the square graph paper, we should expect pi/4
of them to fall *within* the circle as opposed to *outside* it. If we
add *many* random points to the graph paper and keep a count of (a) how many
we add and (b) for how many x<sup>2</sup> + y<sup>2</sup> is less than 1, we
can divide the latter by the former and then multiply by 4 to get an approximate
value of pi.

## License

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org>
