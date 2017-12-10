---
title: ম্যাক-এ সেটআপ  
isChild: true
anchor:  mac_setup
---

## ম্যাক-এ সেটআপ   {#mac_setup_title}

ম্যাকের OS X ভার্সন থেকে পিএইচপি প্রিপ্যাকেজ আকারেই দেয়া থাকে। কিন্তু সেখানে আপনি পিএইচপি এর সর্বশেষ ভার্সন পাবেন না। যেমন,  Mavericks এর সাথে 5.4.17, Yosemite এ 5.5.9, El Capitan এ  5.5.29 এবং  Sierra এর সাথে 5.6.24 দেয়া থাকে। কিন্তু যেহেতু এখন PHP এর 7.1 রিলিজ হয়ে গেছে সেহেতু পুরনো ভার্সনগুলো না ইউজ করে এটাই ইউজ করা উচিত। 

ম্যাক এ কয়েকটি উপায়ে পিএইচপি ইনস্টল করা যায়। তো চলুন, দেখি নেই উপায়গুলোঃ

### Homebrew এর মাধ্যমে ইনষ্টল 

MAC এ পিএইচপি ইনস্টল করার জন্য  [Homebrew] একটি অসাধারণ টুল। এর মাধ্যমে আপনি খুব সহজেই পিএইচপি এর যেকোন ভার্সন ও বিভিন্ন ধরনের এক্সটেনশন ইনস্টল করতে পারবেন।   

[Homebrew PHP] এই রিপোজিটরিতে Homebrew এর বিভিন্ন "formulae" দেয়া আছে যা আপনাকে পিএইচপি Install করতে সাহায্য করবে। 

এই মুহূর্তে, আপনি  `php53`, `php54`, `php55`, `php56`, `php70`  অথবা `php71` এর মধ্যে যেকোন ভার্সন `brew install` কমান্ডের মাধ্যমে খুব সহজেই ইনস্টল করতে পারবেন। 
Alternatively, you can use [brew-php-switcher][brew-php-switcher] which will switch automatically for you.

### Install PHP via Macports

The [MacPorts] Project is an open-source community initiative to design an
easy-to-use system for compiling, installing, and upgrading either
command-line, X11 or Aqua based open-source software on the OS X operating
system.

MacPorts supports pre-compiled binaries, so you don't need to recompile every
dependency from the source tarball files, it saves your life if you don't
have any package installed on your system.

At this point, you can install `php54`, `php55`, `php56`, `php70` or `php71` using the `port install` command, for example:

    sudo port install php56
    sudo port install php71

And you can run `select` command to switch your active PHP:

    sudo port select --set php php71

### Install PHP via phpbrew

[phpbrew] is a tool for installing and managing multiple PHP versions. This can be really useful if two different
applications/projects require different versions of PHP, and you are not using virtual machines.

### Install PHP via Liip's binary installer

Another popular option is [php-osx.liip.ch] which provides one liner installation methods for versions 5.3 through 7.1.
It doesn't overwrite the PHP binaries installed by Apple, but installs everything in a separate location (/usr/local/php5).

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
