# My OSX Developer box

## Steps

There are a few manual steps required before the automated process can be done.

### Install Command Line Tools

OSX does not include a compiler toolchain (`cc`) by default. We need to
trigger it's installation before install Battleschool

```
$ cc
```

This will trigger Xcode Command Line Tools installer (see screenshots)

Next, we proceed to install `pip` (Python Installer)

### Install Python's pip

OSX do not bundles `pip` with it, just `easy_install`. We will use the later
to bootstrap it.

```
$ sudo easy_install pip
```

You will need to enter your password to complete installation.

### Install battleschool

Now that `pip` is available, we install Battleschool with it:

```
$ sudo pip install battleschool
```

This step will take longer as Battleschool has some dependencies.

## Run against a defined configuration

## Special Note about Alfred

According to [this article](http://support.alfredapp.com/kb:symlinked-apps) is
not possible to use `brew cask alfred link` to find installed applications via
`brew cask`

To work around that issue, you should add default's Caskroom directory inside
Alfred's preferences:

```
/opt/homebrew-cask/Caskroom
```
