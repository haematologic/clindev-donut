
### Clinical Developers Club – Donut challenge ###

**Task** – set by [@stuartbman](https://github.com/stuartbman)

"It's very simple- draw a donut

What is a donut?

 - At it's very least, it consists of 2 concentric circles
 - At it's very most, it is a delicious iced dessert with sprinkles

You can use any programming language to make this, and I will look out for solutions which do one of a few things:

 - Fewest lines of code (not really fair to non-python developers i know, sorry!)
 - Best Donut
 - Most creative solution

This is a bit of a departure from previous data analytics challenges, partly to welcome anyone who hasn't entered challenges before/ has been put of by them, and partly because graphics aren't always something considered in introductory programming courses, but are important to bear in mind!
This challenge is actually not my own, but comes from a GCHQ recruiting event I was at 2 years ago. I won this challenge in the first category, if anyone beats me I will buy them a drink at our future meetup!
Same deadline applies- I will look through the solutions on Sunday and feedback and choose the best ones. I'll be about to answer any questions intermittently.

EDIT:
Okay honestly, if anyone can make a coding solution that is better than 78 bytes filesize I will send them a box of krispy kreme donuts"

**Solutions** below, written in **[Processing](https://en.wikipedia.org/wiki/Processing_%28programming_language%29)**, an open source language with minimal IDE and simple syntax available [here](https://processing.org/)

Donut (70 bytes)
<pre>fill(#FFB6C1);ellipse(50,50,55,55);fill(#CCCCCC);ellipse(50,50,25,25);</pre>

And rendered here http://studio.sketchpad.cc/SMo3UzuhEu

Minimal donut (52 bytes)
<pre>ellipse(50,50,50,50);fill(200);ellipse(50,50,22,22);</pre>

This one is covered in white icing, rendered here http://studio.sketchpad.cc/VHWc7L4Yfx

Super-minimal donut (43 bytes)
<pre>fill(200);strokeWeight(3);ellipse(9,9,9,9);</pre>

This one is super-miniature, covered in 99% cocoa dark choc… http://studio.sketchpad.cc/BzHjsPgmJx

And here is **Python 3** answer (75 bytes) that prints a donut bitmap – depending on your preferred resolution and if non vectors allowed!

<pre>d=[28,34,73,85];print('\n'.join(['{:07b}'.format(b) for b in d+d[-2::-1]]))</pre>

Editable **[here](https://repl.it/KQc8)**

This prints a donut in a 7x7 grid by parsing a string of ints into their binary equivalent.
For each int '{:07b}'.format(int) returns the 0-padded 7-bit long binary representation of the int.
To save space, the string is made of two arrays 'd', concatenated d+d[-2::-1].
The second half the string is formed by is an inverse slice of the first [::-1] and sliced minus the first char [-2::] to avoid repeating the middle '0'.