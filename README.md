# LIMP
This script compiles a given LaTeX file and parses the output for any missing
packages and then tries to install those packages. It currently only supports
DNF-based distributions (in particular Fedora).
LIMP stands for "Latex Install Missing Packages".

## Usage
If you have a LaTeX file `mytex.tex` that uses packages that you do not have installed,
simply run

    $ ./limp mytex.tex

The script will try to compile `mytex.tex`, and if the compilation fails due to
a missing package, it will install that package, and re-run the compilation,
until it succeeds or fails due to some other error.
