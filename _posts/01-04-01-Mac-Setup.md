---
isChild: true
anchor:  mac_setup
---

 ## Mac Setup {#mac_setup_title}
 
OS X komt standaard met PHP. Normaal gezien is deze versie iets ouder dan de laatste stabiele versie. Mountain Lion heeft 5.3.10. Mavericks heeft 5.4.17 en Yosemite heeft 5.5.9, echter zijn deze versies vaak net iets te oud en daarom vaak niet goed genoeg.
 
Er zijn verschillende manieren om PHP op OS X te installeren.

### Install PHP via Homebrew

[Homebrew] is a powerful package manager for OS X, which can help you install PHP and various extensions easily.
[Homebrew PHP] is a repository that contains PHP-related "formulae" for Homebrew, and will let you install PHP.

At this point, you can install `php53`, `php54`, `php55` or `php56` using the `brew install` command, and switch
between them by modifying your `PATH` variable. Alternatively you can use [brew-php-switcher][brew-php-switcher] which will switch automatically for you.

//DUTCH TRANSLATION:
### PHP installeren via Homebrew

[Homebrew] is een krachtige package manager voor OS X, die het je gemakkelijk maakt om PHP en verschillende extensies te installeren. [Homebrew PHP] is een repository die een PHP-gerelateerde "formulae" voor Homebrew bevat.

Momenteel kan je `php53`, `php54`, `php55` of `php56` installeren, door gebruik te maken van het `brew install` commando. Door je `PATH` variabele te veranderen kan je schakelen tussen verschillende versies. Als alternatief kan je [brew-php-switcher][brew-php-switcher] gebruiken die automatisch voor je schakelt.

### Install PHP via Macports

The [MacPorts] Project is an open-source community initiative to design an
easy-to-use system for compiling, installing, and upgrading either
command-line, X11 or Aqua based open-source software on the OS X operating
system.

MacPorts supports pre-compiled binaries, so you don't need to recompile every
dependencies from the source tarball files, it saves your life if you don't
have any package installed on your system.

At this point, you can install `php53`, `php54`, `php55` or `php56` using the `port install` command, for example:

    sudo port install php54
    sudo port install php55

And you can run `select` command to switch your active php:

    sudo port select --set php php55

### Install PHP via phpbrew

[phpbrew] is a tool for installing and managing multiple PHP versions. This can be really useful if two different
applications/projects require different versions of PHP, and you are not using virtual machines.

### Install PHP via Liip's binary installer
Another popular option is [php-osx.liip.ch] which provides one liner installation methods for versions 5.3 through 5.6.
It doesn't overwrite the php binaries installed by Apple, but installs everything in a separate location (/usr/local/php5).

### Compile from Source

Another option that gives you control over the version of PHP you install, is to [compile it yourself][mac-compile].
In that case be sure to have installed either [Xcode][xcode-gcc-substitution] or Apple's substitute
["Command Line Tools for XCode"] downloadable from Apple's Mac Developer Center.

### All-in-One Installers

The solutions listed above mainly handle PHP itself, and do not supply things like Apache, Nginx or a SQL server.
"All-in-one" solutions such as [MAMP][mamp-downloads] and [XAMPP][xampp] will install these other bits of software for
you and tie them all together, but ease of setup comes with a trade-off of flexibility.


[Homebrew]: http://brew.sh/
[Homebrew PHP]: https://github.com/Homebrew/homebrew-php#installation
[MacPorts]: https://www.macports.org/install.php
[phpbrew]: https://github.com/phpbrew/phpbrew
[php-osx.liip.ch]: http://php-osx.liip.ch/
[mac-compile]: http://php.net/install.macosx.compile
[xcode-gcc-substitution]: https://github.com/kennethreitz/osx-gcc-installer
["Command Line Tools for XCode"]: https://developer.apple.com/downloads
[mamp-downloads]: http://www.mamp.info/en/downloads/
[xampp]: http://www.apachefriends.org/en/xampp.html
[brew-php-switcher]: https://github.com/philcook/brew-php-switcher
