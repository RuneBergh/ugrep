ugrep predefined patterns
=========================

This directory contains a collection of patterns that are helpful to search
source code files.  Use ugrep option `-f` to specify one or more pattern files
to use for searching these patterns in files.

The list of patterns defined in this directory will expand over time.

For example, to display class definitions in C++ files in the working directory

    ugrep -r -o -tc++ -f c++/classes

To display Java identifiers (Unicode) with the line numbers of the matches, but
skipping all matches of identifiers in comments and strings:

    ugrep -r -n -o -f java/names -f java/zap_comments -f java/zap_strings

Some patterns automatically enable ugrep option `-o` to match multiple lines.
These pattern files start with `###-o` to enable option `-o` that is required
to match the pattern across multiple lines.  For example, strings and comments
may span multiple lines, such as Python docstrings, requiring option `-o`.

Empty lines and lines starting with a `#` are ignored.

Patterns requiring Unicode matching are placed in Unicode mode with `(?u:X)`,
just in case to prevent ugrep option -U from disabling them.

We love your contributions to this effort! ❤️

**If you encounter a problem with a pattern or you discover a bug in a pattern,
please open an issue at GitHub https://github.com/Genivia/ugrep/issues**

