# Teacher Desk

---

[![netlify badge](https://api.netlify.com/api/v1/badges/416b8ca3-82db-470f-9adf-a6d06264ca75/deploy-status)](https://app.netlify.com/sites/mystifying-keller-ab5658/deploys) [![Build Status](https://travis-ci.com/skeptycal/.dotfiles.svg?branch=dev)](https://travis-ci.com/skeptycal/.dotfiles) [![test coverage](https://img.shields.io/badge/test_coverage-100%25-6600CC.svg?logo=Coveralls&color=3F5767)](https://coveralls.io) [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/3454/badge)](https://bestpractices.coreinfrastructure.org/projects/3454)

[![GitHub Pipenv locked Python version](https://img.shields.io/badge/Python-3.8-yellow?color=3776AB&logo=python&logoColor=yellow)](https://www.python.org/) [![nuxt.js](https://img.shields.io/badge/nuxt.js-2.10.2-35495e?logo=nuxt.js)](https://nuxtjs.org/) [![macOS Version](https://img.shields.io/badge/macOS-10.15%20Catalina-orange?logo=apple)](https://www.apple.com)

[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?logo=prettier)](https://github.com/prettier/prettier) [![License](https://img.shields.io/badge/License-MIT-darkblue)](https://skeptycal.mit-license.org/1976/) [![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v1.4%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md)

![Twitter Follow](https://img.shields.io/twitter/follow/skeptycal.svg?style=social) ![GitHub followers](https://img.shields.io/github/followers/skeptycal.svg?label=GitHub&style=social)

## Description

This is my software development setup for a MacBook Pro (mid-2015, 16g ram, 256g SSD). It is the setup I currently use and may change frequently. I am a dabbler in many arts ... and far from expert in most areas. Take it for what it is worth to you.

**Please feel free to offer suggestions and changes** (contribution instructions below). I have been coding for many years, but mostly as a side activity ... as a tool to assist me in other endeavors ... so I have not had the 'hard time' invested of constant coding that many of you have.

> Copyright © 2018-2019 [Michael Treanor](https:/skeptycal.github.com)

> Many original settings © 2018 [Mathias Bynens](https://mathiasbynens.be/)

> [MIT License](https://opensource.org/licenses/MIT) - enjoy ...

## Installation

**Warning:** If you want to use this setup, you should fork this repository, review the code, and make changes to suit your needs.

If you aren't sure, don't use it! This setup works for me for what I do. Don’t blindly use my settings unless you know what that entails. It could make your system inoperable or at least very annoying to use! Use at your own risk!

### Using Git and the bootstrap script

You can clone the repository wherever you want. (I like to keep it in `~/.dotfiles`) The bootstrapper script will pull in the latest version and copy the files to your home folder.

```bash
git clone https://github.com/skeptycal/dotfiles.git && cd .dotfiles && source bootstrap.sh
```

To update, `cd` into your local `.dotfiles` repository and then:

```bash
source bootstrap.sh
```

Alternatively, to update while avoiding the confirmation prompt:

```bash
set -- -f; source bootstrap.sh
```

### Specify the `$PATH`

If `~/.path` exists, it will be sourced along with the other files, before any feature testing (such as [detecting which version of `ls` is being used](https://github.com/mathiasbynens/dotfiles/blob/aff769fd75225d8f2e481185a71d5e05b76002dc/.aliases#L21-26)) takes place.

Here’s an example `~/.path` file that adds `/usr/local/bin` to the `$PATH`:

```bash
export PATH="/usr/local/bin:$PATH"
```

### Add custom commands without creating a new fork

If `~/.extra` exists, it will be sourced after the other files. You can use this to add a few custom commands without the need to fork this entire repository, or to add commands you don’t want to commit to a public repository.

My `~/.extra` looks something like this:

```bash
# Git credentials
# Not in the repository, to prevent people from accidentally committing under my name
GIT_AUTHOR_NAME="Michael Treanor"
GIT_COMMITTER_NAME="$GIT_AUTHOR_NAME"
git config --global user.name "$GIT_AUTHOR_NAME"
GIT_AUTHOR_EMAIL="skeptycal@gmail.com"
GIT_COMMITTER_EMAIL="$GIT_AUTHOR_EMAIL"
git config --global user.email "$GIT_AUTHOR_EMAIL"
```

Since it is sourced last, you could also use `~/.extra` to override settings, functions and aliases from my dotfiles repository. It’s probably better to [fork this repository](https://github.com/mathiasbynens/dotfiles/fork) instead, though.

### Sensible macOS defaults

When setting up a new Mac, you may want to set some sensible macOS defaults:

```bash
./.macos
```

### Install Homebrew formulae

When setting up a new Mac, you may want to install some common [Homebrew](https://brew.sh/) formulae (after installing Homebrew, of course):

```bash
./brew.sh
```

Some of the functionality of these dotfiles depends on formulae installed by `brew.sh`. If you don’t plan to run `brew.sh`, you should look carefully through the script and manually install any particularly important ones. A good example is Bash/Git completion: the dotfiles use a special version from Homebrew.

## Feedback

Suggestions/improvements
[welcome](https://github.com/skeptycal/dotfiles/issues)!

## Author

[![twitter/skeptycal](https://s.gravatar.com/avatar/b939916e40df04f870b03e0b5cff4807?s=80)](http://twitter.com/skeptycal 'Follow @skeptycal on Twitter')

[**Michael Treanor**](https://www.skeptycal.com)

## Thanks to…

-   @ptb and [his _macOS Setup_ repository](https://github.com/ptb/mac-setup)
-   Anyone who [contributed a patch](https://github.com/mathiasbynens/dotfiles/contributors) or [made a helpful suggestion](https://github.com/mathiasbynens/dotfiles/issues)

# Kite Python Plugin for Visual Studio Code

Kite is an AI-powered programming assistant that helps you write Python code inside Visual Studio Code. Kite helps you write code faster by showing you the right information at the right time. Learn more about how Kite heightens VS Code's capabilities at https://kite.com/integrations/vs-code/.

At a high level, Kite provides you with:

-   🧠 **[Line-of-Code Completions](https://kite.com/blog/product/launching-line-of-code-completions-going-cloudless-and-17-million-in-funding/)** powered by machine learning models trained on the entire open source code universe
-   📝 **[Intelligent Snippets](https://kite.com/blog/product/announcing-intelligent-snippets-for-python/)** that automatically provide context-relevant code snippets for your function calls
-   🔍 **[Instant documentation](https://kite.com/copilot/)** for the symbol underneath your cursor so you save time searching for Python docs

## Requirements

-   macOS 10.11+, Windows 7+ or Linux
-   Visual Studio Code v1.28.0+
-   [Kite Engine](https://kite.com/)

Use another editor? Check out [Kite’s other editor integrations](https://kite.com/integrations/).

## Installation

### Installing the Kite Engine

The [Kite Engine](https://kite.com/) needs to be installed in order for the package to work properly. The package itself
provides the frontend that interfaces with the Kite Engine, which performs all the code analysis and machine learning 100% locally on your computer (no code is sent to a cloud server).

**macOS Instructions**

1. Download the [installer](https://kite.com/download/) and open the downloaded `.dmg` file.
2. Drag the Kite icon into the `Applications` folder.
3. Run `Kite.app` to start the Kite Engine.

**Windows Instructions**

1. Download the [installer](https://kite.com/download/) and run the downloaded `.exe` file.
2. The installer should run the Kite Engine automatically after installation is complete.

**Linux Instructions**

1. Visit https://kite.com/linux/ to install Kite.
2. The installer should run the Kite Engine automatically after installation is complete.

### Installing

Basic ...

Alternatively, you have 2 options to manually install the package:

1. Search for "Kite" in VS Code's built-in extension marketplace and install from there.
2. Run the command `code --install-extension kiteco.kite` in your terminal.

[Learn about the capabilities Kite adds to VS Code.](https://kite.com/integrations/vs-code/)

## Usage

The following is a brief guide to using Kite in its default configuration.

### Feature1

Hover your mouse cursor over a symbol to view a short summary of what the symbol represents.

(example)

### Feature2

Click on the `Docs` link in the hover popup to open the documentation for the symbol inside the Copilot, Kite's standalone
reference tool.

(example)

### Feature3

If a `Def` link is available in the hover popup, clicking on it will jump to the definition of the symbol.

### (example with pic)

example ... stuff ... Kite's
autocompletions are all labeled with the `⟠` symbol.

![sample](images/vscode_python.png)

### (example 2 with pic)

2nd example ... stuff ... Kite's
autocompletions are all labeled with the `⟠` symbol.

![sample](images/vscode_python.png)

> **Note:** If you have the Microsoft Python extension installed, Kite will
> _not_ be able to show you information on function signatures.

### Commands

Cool looking table ...

| Command                | Description                                                            |
| :--------------------- | :--------------------------------------------------------------------- |
| `kite.open-copilot`    | Open the Copilot                                                       |
| `kite.docs-at-cursor`  | Show documentation of the symbol underneath your cursor in the Copilot |
| `kite.engine-settings` | Open the settings for the Kite Engine                                  |
| `kite.help`            | Open Kite's help website in the browser                                |

## Contact Us

Feel free to contact us with bug reports, feature requests, or general comments.

Happy coding!

---

#### About Kite

Kite is built by a team in San Francisco devoted to making programming easier and more enjoyable for all. Follow Kite on [Twitter](https://twitter.com/skeptycal) and get the latest news and programming tips on the [Skeptycal Blog](https://medium.com/@Skeptycal).
