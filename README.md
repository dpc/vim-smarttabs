# Vim Smart Tabs

This is a github copy of [Smart Tabs : Use tabs for indent, spaces for alignment](http://www.vim.org/scripts/script.php?script_id=231) originally created by Michael Geddes.

It seems author is not actively maintaining it anymore, and trivial bugs are not
being fixed, so for convenience of mine and other people I've gave it a new
home. I'm not a skilled Vim dev, so feel free to contact me to take it over.

## Introduction (adopted from from vim.org)

There are many different arguments about tabs and stuff.  My current personal
preference is a choice of tabbing that is independent of anybody's viewing
setting.

For the beginning of the line, this means we can use <tabs> which will expand
whatever the reader wants it to.  Trying to line up tabs at the end of the line
is a little trickier, and making a few assumptions, my preference is to use
spaces there.

This script allows you to use your normal tab settings for the beginning of the
line, and have tabs expanded as spaces anywhere else.  This effectively
distinguishes `indent` from `alignment`.

* `<tab>`  Uses editor tab settings to insert a tab at the beginning of the
  line (before the first non-space character), and inserts spaces otherwise.
* `<BS>`  Uses editor tab settings to delete tabs or `expanded` tabs ala
  `smarttab`

`:RetabIndent[!] [tabstop]` - This is similar to the `:retab` command, with the
exception that it affects all and only whitespace at the start of the line,
changing it to suit your current (or new) `tabstop` and `expandtab` setting.
With the bang (!) at the end, the command also strips trailing  whitespace.

## Installation:

### With Patogen:

```sh
mkdir -p ~/.vim/bundle && cd ~/.vim/bundle && git clone https://github.com/dpc/vim-smarttabs.git
```

Then run `:Helptags` from within vim to add helptags for the documentation.

### Using vim-plug:

Add this to your `init.vim` or `.vimrc`:
```vim
Plug 'dpc/vim-smarttabs'
```

Then run `:PlugInstall` from within vim.

### Manually:

Just copy `smarttabs.vim` into `~/.vim/plugin`. Notice that this will not
install the documentation.
