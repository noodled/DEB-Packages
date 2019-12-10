**NOTE:** _All packages are built from master branches._

# Information

Thank you for checking out these Debian packages (info [here](https://www.debian.org/doc/manuals/debian-faq/ch-pkg_basics.en.html)) I've built for Debian- and Ubuntu-based distributions of Linux. Continue reading to learn of anything worth mentioning here.

You'll find packages here typically (but not exclusively) from [Extra](https://github.com/terminalforlife/Extra) and [PerlProjects](https://github.com/terminalforlife/PerlProjects) repositories.

The packages here can be downloaded and installed with a one-liner in a terminal, or by using your browser then a utility like `gdebi` (info [here](https://simple.wikipedia.org/wiki/Gdebi)) which has a GUI. See below for the aforementioned one-liner.

##### Install via Terminal

Here is a basic example of how to install the `apt-undo-install` Debian package from a terminal, by using the below one-liner. Ensure there is no file in the current directory with the same name present, otherwise it would be overwritten.

```bash
if wget -q https://raw.githubusercontent.com/terminalforlife/DEB-Packages/master/apt-undo-install/apt-undo-install_2019-05-09_all.deb; then sudo dpkg -i apt-undo-install_2019-05-09_all.deb && rm apt-undo-install_2019-05-09_all.deb; fi
```

If you don't have Wget, try Curl, by replacing `wget -q` with `curl -s`. The `-q` or `-s` option just tells these programs to hush, as they produce a lot of output.

Before installing any of these packages, you're welcome to check their hashes ([128-bit MD5 hashes](https://en.wikipedia.org/wiki/Md5sum)), in an effort to avoid executing files with which have been tampered. The hashes will (hopefully always) be stored in [this](md5sum) file.

To check a hash for any number of the packages retrieved from here, run the below one-liner on a terminal, whilst in the same directory into which you downloaded your chosen package(s).

```bash
wget -qO - https://raw.githubusercontent.com/terminalforlife/DEB-Packages/master/md5sum | md5sum -c --ignore-missing
```

Example of a successful check:

```
lsbins_2019-05-09_all.deb: OK
purgerc_2019-05-09_all.deb: OK
ubuntu-syschk_2019-10-27_all.deb: OK
wcdl_2019-05-11_all.deb: OK
```

# Disclaimer

This GitHub repository is for convenience only.

The contents of each DEB package falls under the license respective to its original repository, as found under the GitHub user 'terminalforlife'. Use of each DEB package therefore comes with the same limitations described in the associated 'LICENSE' file.

Some versions of programs within this directory may not be the latest version available up one level, but the user may decide to install them manually. If you do, `/usr/bin/` is the intended (but not required) destination, so ensure correct and safe permissions and ownership attributes of all transferred files.
