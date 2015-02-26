Coconut
=======

Coconut is a simple, modern, developer-friendly scripting language that compiles to Python, built for functional programming.

Installation
------------

Enter in console::

    pip install coconut

Command Line
------------

usage:
  ``coconut [-h] [-v] [-s] [-r] [-i] [-d] [-c ...] [--autopep8 ...] [source] [dest]``

positional arguments:
  :source:            path to the coconut file/module to compile
  :dest:              destination directory for compiled files (defaults to the source directory)

optional arguments:
  -h, --help          show this help message and exit

  -v, --version       print coconut and python version information

  -s, --strict        enforce code cleanliness standards

  -r, --run           run the compiled source instead of writing it

  -i, --interact      force the interpreter to start (otherwise starts if no other command is given)

  -d, --debug         show compiled python being executed

  -c, --code          run code passed in as string (terminates arg list)

  --autopep8          use autopep8 to format compiled code (terminates arg list)

Syntax
------

Coconut is based on Python 3 syntax and compiles to Python 3 code. Coconut makes significant changes from Python 3 syntax, however:

- New operators:
    - compose: ``..`` (in-place: ``..=``)
    - partial: ``$``
    - pipeline: ``|>`` (in-place: ``=>``)
    - lambda: ``->``
    - chain: ``::`` (in-place: ``::=``)
- New syntax:
    - infix function calling: new ``6 `mod` 3`` syntax
    - operator functions: new ``(+)`` syntax
    - function definition: alternative ``f(x) = x`` syntax
    - non-decimal integers: alternative ``10110_2`` syntax
- Changed syntax:
    - unicode symbols: supports unicode alternatives for most symbols
    - lambda keyword: removed (use the lambda operator instead)
- New built-ins:
    - right reduce: ``reduce``
    - zip with function: ``zipwith``
    - tail recursion elimination: ``recursive``
- New constructs: (planned)
    - operator [re]definition
    - pattern matching