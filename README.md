labelpin
========

The right way to label figures in LaTeX is to do so within the TeX
file itself so that the fonts match and it's easy to move/change the
labels without access to the program that originally generated the
image files. Colin Rourke's [pinlabel.sty] is a good way to do this
and is used by the [MSP journals]. The hard part is figuring out the
coordinates for the labels without a lot of guesswork. Pete Storm
wrote [pinlabeler] which makes this trivially easy, but unfortunately
it doesn't work naturally with Mac OS X. Therefore I wrote
**labelpin** which is less sophisticated than pinlaber, but works
on OS X, Linux, and Windows. It's just a simple Python script, so
there's no need to compiler anything. Installation instructions are at
the top of file, but on OS X all you should need to do is put it in
your path and make it executable (`chmod +x labelpin`). For usage
instructions, do `labelpin -h`.


Alternatives to pinlabel.sty include [overpic], WARMReader, the
import environment of [xypic], and [TikZ]. It's easy to modify the
`labelpin` script to handle any of these, and I have done so for xypic
and TikZ in the form of `labelxy` and `labeltikz`. The TikZ version
needs the (tiny) TeX package `tikzoverlay.sty` included in this
repository.

Personally, I use the TikZ variant since it's easy to add additional
graphical elements beyond just labels. 

[pinlabel.sty]: http://www.ctan.org/tex-archive/help/Catalogue/entries/pinlabel.html
[MSP journals]: http://mathscipub.org/
[pinlabeler]: http://hans.math.upenn.edu/~pstorm/pinlabeler.html
[xypic]: http://www.ctan.org/tex-archive/help/Catalogue/entries/xypic.html
[overpic]: http://www.ctan.org/tex-archive/help/Catalogue/entries/overpic.html
[TikZ]: http://www.ctan.org/pkg/pgf
