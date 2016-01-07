Bobby.js
========

About
-----
Render document as Github-styled Markdown when viewed in a browser.

Render document as ASCII Markdown when viewed in a text editor.

Do not pass go, do not run external tool.


How to use
----------
1. Fork this repo.
2. Copy the last line containing a "&lt;script&gt;"-tag from this file to the end of another document in the same directory.
3. If you care for latin1 characters, make sure you do not truncate the magic string below.
4. Name the file with an .md extension so syntax highlightning gets enabled in vim (or $EDITOR)
5. Create a symlink with the extension .html so it renders ok in a browser.
6. ???
7. Profit!

ISO8859-1 encoding
------------------
Non-english speakers beware: the markup file must be encoded as ISO8859-1 as the browsers seems to fall back to ISO8859-1.


iconv(1) can be used to convert a file from UTF-8 to ISO8859-1:
    
     iconv -f UTF-8 -t ISO8859-1 utf_file.txt | tee iso_file.txt

Syntax highlightning
--------------------
The syntax highlightning is not exactly like Github, but retains the colors where possible:

    #include <stdio.h>
    int main(int argc, char **argv)
    {
        printf("hello world!\n");
    }

Acknowledgement
---------------
Fork of [jr](http://github.com/xeoncross/jr), this version mainly removes the footer requirement and has a Github like layout.

[Donate Stellar](https://www.stellar.org) to xeoncross

License
-------
No further restrictions from Thomas Eriksson

MIT License with <3 from [David Pennington](http://davidpennington.me)

Bugs
----
Yes.

<script src="js/bobby.js" iso8859-1_magic="едц"></script>
