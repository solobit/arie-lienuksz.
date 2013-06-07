
Toolkit
=======

Names of household appliances used in my everyday hacking 'n slackin.

Usually available through the [official repositories][offrepos], those are:
* core
* extra
* community
* multilib
* testing (community-testing or multilib-testing)

Another source of much software, if not the most, is by using the
[Arch User Repository][aur] and `makepkg` to custom configure and build with
settings optimized for your machine.

Official channels provided software is much faster to install due to the fact
that it delivers pre-compiled binaries most commonly found on the average Linux
slash Archer pc's. Examples are Google Chrome or OpenOffice (imagine having to
compile these yourself - some will take more than a day).

The process of installing packages through the AUR requires either a internet
connection and browser (download the file required, a bash script named PKGBUILD)
or using the, often prefered, convenience method of a query/download tool named
`yaourt`.

It is probably best to always check the scripts, some common causes of failure
to build originate here, not in the actual software.

* first check the comments in the AUR forum if someone has the same problem
* if it isn't reported/solved yet, and you do, leave them a note in that forum
* remove i686 from the ARCH array (or x86\_64 if you run a 386 processor)
* add single quotes to the elements (e.g. ARCH=('x86\_64' not ARCH=(x86\_64))
* remove a dependency if it can't be found by the downloader or rename if wrongly
* any URLs that are dead, try to provide one thats alive (prefered) or remove

There are many things that can go wrong with building software using the GNU
Autotools tool-chain. It is very sensitive to slight changes in versions although,
it has been pretty much unchanged for years so this problem has decreased
significantly the past few years (this used to be a bigger problem). If the
software you try to install relies on outdated automake, autoconf, libtool or m4
you might be asking yourself why you really need it and if there aren't other
(better, newer etc.) alternatives.

It is also possible that the package is built, not using autotools but instead
which relies on more recent developments. Do note that the trade-off for GNU
Autotools generated projects is portability (it will run nearly everywhere) which
may not be the case with, say `QMake` or `CMake` or `Scons`. Most of these tools
try to bridge a gap, fix a shortcomming of automake (usually less obscure) but
there are trade-offs. Scons is in Python, a lot friendlier than Bash or any shell
script for that matter, but it's not standard for most systems and you might need
to bootstrap an installation of the correct python version before you can
continue. For languages like C/C++ this is not an option anyway but CMake, a nice
tool that makes it easier to successfully build, does not offer as much portable
assurance as GNU Autotools do.

[Read more if you will here](http://freecode.com/articles/stop-the-autoconf-insanity-why-we-need-a-new-build-system)


[aur]: <https://aur.archlinux.org/>
[offrepos]: <https://wiki.archlinux.org/index.php/Official_Repositories>



