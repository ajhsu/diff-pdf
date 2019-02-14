*Note: this repository is provided **as-is** and the code is not being actively
developed. If you wish to improve it, that's greatly appreciated: please make
the changes and submit a pull request, I'll gladly merge it or help you out
with finishing it. However, please do not expect any kind of support, including
implementation of feature requests or fixes. If you're not a developer and/or
willing to get your hands dirty, this tool is probably not for you.*

## Usage

diff-pdf is a tool for visually comparing two PDFs.

It takes two PDF files as arguments. By default, its only output is its return
code, which is 0 if there are no differences and 1 if the two PDFs differ. If
given the `--output-diff` option, it produces a PDF file with visually
highlighted differences:

```
$ diff-pdf --output-diff=diff.pdf a.pdf b.pdf
```

## Compiling from sources

The build system uses Automake and so a Unix or Unix-like environment (Cygwin
or MSYS) is required. Compilation is done in the usual way:

```
$ ./bootstrap
$ ./configure
$ make
$ make install
```

(Note that the first step, running the `./bootstrap` script, is only required
when building sources checked from version control system, i.e. when `configure`
and `Makefile.in` files are missing.)

As for dependencies, diff-pdf requires the following libraries:

- wxWidgets >= 3.0
- Cairo >= 1.4
- Poppler >= 0.10

#### Ubuntu:

```
$ sudo apt-get install make automake g++
$ sudo apt-get install libpoppler-glib-dev poppler-utils libwxgtk3.0-dev
```

## Installing

On Unix, the usual `make install` is sufficient.