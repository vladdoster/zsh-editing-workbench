![zew logo](http://imageshack.com/a/img924/5479/AiIW6X.gif)

# Zsh Editing Workbench [![Gitter][gitter-image]][gitter-link]

Also check out [![ZNT](http://imageshack.com/a/img910/3618/oDHnuR.png) Zsh Navigation Tools](https://github.com/zdharma-continuum/zsh-navigation-tools)
and [![ZCA](http://imageshack.com/a/img911/8084/qSpO8a.png) Zsh Command Architect](https://github.com/zdharma-continuum/zsh-cmd-architect)


Incremental history _word_ completing (started with `Alt-h/H` or `Option-h/H` on Mac):

![zew](http://imageshack.com/a/img907/1065/lJmzII.gif)

Swapping, copying, deleting shell words, also undo:

![zew](http://imageshack.com/a/img908/7765/zpdjOK.gif)

## Installation With [Zinit](https://github.com/zdharma-continuum/zinit)

Add `zinit load zdharma-continuum/zsh-editing-workbench` to `.zshrc`. The config files will be available in `~/.config/zew`.

## Installation With Zgen

Add `zgen load zdharma-continuum/zsh-editing-workbench` to `.zshrc` and issue a `zgen reset` (this assumes that there is a proper `zgen save` construct in `.zshrc`).
The config files will be available in `~/.config/zew`.

## Installation With Antigen
Add `antigen bundle zdharma-continuum/zsh-editing-workbench` to `.zshrc`. There also
should be `antigen apply`. The config files will be in `~/.config/znt`.

## Manual Installation

After extracting `ZEW` to `{some-directory}` add following two lines
to `~/.zshrc`:

```zsh
fpath+=( {some-directory} )
source "{some-directory}/zsh-editing-workbench.plugin.zsh"
```

As you can see, no plugin manager is needed to use the `*.plugin.zsh`
file. The above two lines of code are all that almost **all** plugin
managers do. In fact, what's actually needed is only:

```zsh
source "{some-directory}/zsh-editing-workbench.plugin.zsh"
```

because `ZEW` detects if it is used by **any** plugin manager and can
handle `$fpath` update by itself.

## Introduction

Organized shortcuts for various command line editing operations, plus new
operations (e.g. incremental history word completion).

![zew refcard](http://imageshack.com/a/img922/1959/4gXU1R.png)

# Configuring terminals

**XTerm**

To make `Alt` key work like expected under `XTerm` add `XTerm*metaSendsEscape: true` to your resource file, e.g.:

```
echo 'XTerm*metaSendsEscape: true' >> ~/.Xresources
```

[gitter-image]: https://badges.gitter.im/zdharma-continuum/community.svg
[gitter-link]: https://gitter.im/zdharma-continuum/community
