Sumerian: `apertium-sux`
===============================================================================

This is an Apertium monolingual language package for Sumerian. What
you can use this language package for:

* Morphological analysis of Sumerian
* Morphological generation of Sumerian
* Part-of-speech tagging of Sumerian

Requirements
-------------------------------------------------------------------------------

You will need the following software installed:

* autoconf
* automake
* pkg-config
* lttoolbox (>= 3.5.1)
* apertium (>= 3.6.1)
* vislcg3 (>= 1.3.1)
* hfst (>= 3.15.1)
* lexd (>= 0.0.1)

If this does not make any sense, we recommend you look at: apertium.org.

Compiling
-------------------------------------------------------------------------------

Given the requirements being installed, you should be able to just run:

```bash
$ autoreconf -fvi
$ ./configure
$ make
```

You can use `./autogen.sh` instead of `autoreconf` and `./configure` if you're compiling
from source.

If you're doing development, you don't have to install the data, you
can use it directly from this directory.

If you are installing this language package as a prerequisite for an
Apertium translation pair, then do (typically as root / with sudo):

```bash
$ make install
```

You can use a `--prefix` with `./configure` to install as a non-root user,
but make sure to use the same prefix when installing the translation
pair and any other language packages.

If any of this doesn't make sense or doesn't work, see https://wiki.apertium.org/wiki/Install_language_data_by_compiling

Testing
-------------------------------------------------------------------------------

If you are in the source directory after running make, the following
commands should work:

```console
$ echo "TODO: test sentence" | apertium -d . sux-morph
TODO: test analysis result

$ echo "TODO: test sentence" | apertium -d . sux-tagger
TODO: test tagger result
```

Files and data
-------------------------------------------------------------------------------


* [`apertium-sux.sux.lexd`](apertium-sux.sux.lexd) - Morphotactic dictionary
* [`apertium-sux.sux.twol`](apertium-sux.sux.twol) - Morphophonological rules
* [`apertium-sux.sux.rlx`](apertium-sux.sux.rlx) - Constraint Grammar disambiguation rules
* [`apertium-sux.post-sux.dix`](apertium-sux.post-sux.dix) - Post-generator
* [`sux.prob`](sux.prob) - Tagger model
* [`apertium-sux.sux.udx`](apertium-sux.sux.udx) - Mappings from Apertium tags to Universal Dependencies features
* [`modes.xml`](modes.xml) - Translation modes

For more information
-------------------------------------------------------------------------------

* https://wiki.apertium.org/wiki/Installation
* https://wiki.apertium.org/wiki/apertium-sux

Help and support
-------------------------------------------------------------------------------

If you need help using this language pair or data, you can contact:

* Mailing list: apertium-stuff@lists.sourceforge.net
* IRC: `#apertium` on irc.oftc.net (irc://irc.oftc.net/#apertium)

See also the file [`AUTHORS`](AUTHORS), included in this distribution.
