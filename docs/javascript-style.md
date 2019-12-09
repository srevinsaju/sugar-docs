Code style for Sugar JavaScript development
=====================================

General
-------

* Avoid lines longer than 79 characters

### Javascript

* Make your code conform to JSHint. [See explanation below](#jshint).

* When writing new code, use 4 spaces for indentation, but when editing existing code, use the same indentation style.

The js-beautify tool can be handy for the indentation part. [See
explanation below](#js-beautify).

Here is a good reading about javascript code conventions
<http://javascript.crockford.com/code.html> .

For public and private members of an object, read
<http://javascript.crockford.com/private.html>.  To make the object
available in private members, keep a private variable named **that**:

    var that = this;

Tools
-----

### </a>JSHint

Use JSHint <http://jshint.com/> to check for errors and make the
source compatible with our coding conventions.  The jshint command is
provided by sugar-build.

To check JavaScript code:

    jshint js/main.js

Add it to your editor to ease development.  There are several plugins
at <http://jshint.com/install/> .

### js-beautify

Use js-beautify <https://github.com/einars/js-beautify> to make the
sources compatible with our indentation conventions.  The js-beautify
command is provided by sugar-build.

To clean javascript code:

    js-beautify --replace --good-stuff js/main.js

Warning: the --replace option will modify your source.  But you will
be safe if you are versioning it (we use git for Sugar Web).

It can do HTML as well:

    js-beautify --type html --replace --indent-size 2 index.html

Add it to your editor to ease development.  There are several plugins
at <http://jsbeautifier.org/> .