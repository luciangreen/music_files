# Music Files

Metadata of songs created with Music Composer.

# Getting Started

Please read the following instructions on installing the project to convert and play the music files on your computer.

# Prerequisites

* Use a search engine to find the Homebrew (or other) Terminal install command for your platform and install it, and search for the Terminal command to install swipl using Homebrew and install it or download and install SWI-Prolog for your machine at <a href="https://www.swi-prolog.org/build/">SWI-Prolog</a>.

* You may need to install Gawk using Homebrew.

* Install <a href="https://github.com/soimort/translate-shell">Translation Shell</a> on Mac, etc.
Change line in
```
culturaltranslationtool/ctt2.pl
trans_location("../../../gawk/trans").
```
to correct location of <a href="https://github.com/soimort/translate-shell">trans</a>.

# Mac, Linux and Windows (with Linux commands installed): Prepare to run swipl

* In Terminal settings (Mac), make Bash the default shell:

```
/bin/bash
```

* In Terminal, edit the text file `~/.bashrc` using the text editor Nano:

```
nano ~/.bashrc
```

* Add the following to the file `~/.bashrc`:

```
export PATH="$PATH:/opt/homebrew/bin/"
```

* Link to swipl in Terminal:

```
sudo ln -s /opt/homebrew/bin/swipl /usr/local/bin/swipl
```

# 1. Install manually

* Download:
* <a href="https://github.com/luciangreen/music_files">this repository</a>
* Other repositories that this repository requires are listed in `List-Prolog-Package-Manager/lppm_registry.txt`.

# 2. Or Install from List Prolog Package Manager (LPPM)

* Download the <a href="https://github.com/luciangreen/List-Prolog-Package-Manager">LPPM Repository</a>:

```
mkdir GitHub
cd GitHub/
git clone https://github.com/luciangreen/List-Prolog-Package-Manager.git
cd List-Prolog-Package-Manager
swipl
['lppm'].
lppm_install("luciangreen", "music_files").
../
halt.
```

# Convert meta to mid files

* Enter `cd ../Music-Composer`, `swipl`, then place `*_meta.txt` files in the `meta` folder, enter `['meta2mid.pl'].` and `meta2mid.` and the `*lyrics.txt`, `*.mid` and `*.txt` files will be saved in the `Music-Composer` folder.

* Use free or paid software such as `Switch` (Mac) to convert the `.mid` files to `.mp3` files.

# Versioning

We will use SemVer for versioning.

# Authors

Lucian Green - Initial programmer - <a href="https://www.lucianacademy.com/">Lucian Academy</a>

# License

I licensed this project under the BSD3 License - see the LICENSE.md file for details
