---
layout: splash
permalink: /notes/vim_notes/
title: "Vim Notes"
excerpt: "Yes, this vim, legendary VIM Notes... Seee you soon, more or lesss"
toc: true
author_profile: false
---

# VIM INTRO

## My fealings about vim

- First fealing?! ... like I want to hit someone -.- (specially with mouse)!
- Real programmers should use vim! vi! nano! willpower to >> | << bits!
- I dont want gui, just console, otherwise why to bother when I can use VS, JetBrains with vim mode?
- Maybe not helpful to pick girls -.- ...
- Great for showing off among programmers! I use vim, Ha! I, your granddaddy is awesome! 


# VIM DISTROS

## yavide:
- for c++ dev
- not good for nvim

## spf13-vim:
- cross platform
- allin
- but not good for nvim

## evervim:
- problem in completion on wsl
- great user friendly
- half step in nvim
- 1998 chinese sophomore

## navim:
- based on evervim
- from here I know than .vim config are actually in Python (now its easier)

## rafi/vim-config
- not so userfriendly
- just forkit and do as you please
- problem with rendering of built in theme:
-- trash its theme config file content and put onedark, dracula, etc...

# My REQUIREMENTS FROM VIM DISTRO

## must be:
- nvim (made by Shougo)
- only terminal
- not light, not dark side, grey (dark is ide, light is cmd)
- use Shougo favourite plugins that match nvim perfectly:
-- [why?](http://howivim.com/2016/shougo/)
-- dein
-- denim
-- vimproc.vim
-- denite/unite.vim
-- deoplete.nvim/neocomplete.vim:
--- we do not need YCM when nvim is async as opposite to vim
-- vimshell.vim
-- vimfiler.vim or NERDTree

## optional:
- easy to do user config or fork and reconfig

## winner

- create your own distro based on rafi and navim:
-- fork rafi/vim-config and merge it with navim

# VIM MODIFIED KEYMAP

##how to check keymap:
:verbose nmap <...>

##popular keymap:

nmap <-> fast switch between window area
namp <C-2> jump to next word
nmap <C--> zoom out
namp <C-+> zoom int
nmap <C-q> ...
nmap <C-w> ...
nmap <C-e> ...
nmap <C-r> reload file
nmap <C-t> err: tag bar empty
	 <C-y> ...
	 <C-u> ...
	 <C-i> ...
	 <C-o> 
	 <c,i,d> remove current word
vmap > or < indent left or right 
   
##popular commands	 
:%s/foo/bar/g
Find each occurrence of 'foo' (in all lines), and replace it with 'bar'.
Vim replace:




# VIM CONFIG

## General Info

### Vimrc config syntax is based on python.

### To create list with multilines

list = [
  / line1,
  / line2,
/]

## My plugins

### For conda envs:

cjrh/vim-conda

#### example of usage

```vim

#in vim
:CondaChangeEnv<ENTER>

#in ~/.config/nvim/init.vim
map <F4> :CondaChangeEnv<CR>
```

---

# FOR FUTURE ...

# COMPILATION

## C++

:!gcc -o somename % && ./somename

# VIM KEYMAP

# Cut/Copy/Paste/Modify

## Cut/Delete
+ `dd` Delete current line
+ `#dd` Delete # lines
+ `dw` Delete current word
+ `d$` Delete to end of line
+ `D` Delete to end of line
+ `:#,&d` Delete from line # to &
+ `"[a-zA-Z0-9]dd` Delete line into register [a-zA-Z0-9]
+ `"+dd` Delete line into host clipboard

## Copy/Yank
+ `yy` Yank current line
+ `Y` Yank current line
+ `#yy` Yank # lines
+ `yw` Yank current word
+ `y$` Yank to end of line
+ `y^` Yank to beginning of line
+ `:#,&y` Yank from line # to &
+ `"[a-zA-Z0-9]yy` Yank line into register [a-zA-Z0-9]
+ `"+yy` Yank line into host clipboard

## Paste/Put
+ `p` Put current register at cursor
+ `P` Put current register before cursor
+ `"[a-zA-Z0-9]p` Put register [a-zA-Z0-9] at cursor
+ `"+p` Put text from clipboard at cursor
+ `]p` Put current register WRT indent

## Modify
+ `gUw` Switch case of word to CAPS
+ `guw` Switch case of word to lower
+ `~` Switch case of character under cursor
+ `g~w` Invert case on word
+ `r#` Replace character under cursor with #
+ `ce` Replace from cursor to end of word
+ `c$` Replace from cursor to end of line
+ `C` Replace from cursor to end of line
+ `c#w` Replace # words
+ `ci"` Replace between double quote pair
+ `ci'` Replace between single quote pair
+ `ci)` Replace between () pair
+ `ci]` Replace between [] pair
+ `ci}` Replace between {} pair
+ `ci>` Replace between <> pair
+ `cit` Replace beetween XML/HTML tag pair
+ `<ctrl> A` Increment number under cursor
+ `<ctrl> X` Decrement number under cursor
+ `x` Delete character under cursor
+ `X` Delete character before cursor
+ `>>` Indent entire line
+ `<<` Unindent entire line
+ `==` Autoindent entire line
+ `:reg` View contents of registers

# Code folding
+ `zo` Open fold
+ `zc` Close fold
+ `zr` Reduce fold level
+ `zm` Increase fold level
+ `zR` Reduce all folds
+ `zM` Increase all folds
+ `zj` Move to next fold downwards
+ `zk` Move to next fold upward
+ `zd` Delete fold
+ `zE` Delete all folds
+ `zf#j` Create fold of # lines below cursor
+ `:#,& fold` Create fold beetween line # and &
+ `zfap` Create fold of paragpraph
+ `zfa}` Create fold in {} brackets
+ `zfa)` Create fold in () brackets
+ `zfa]` Create fold in [] brackets
+ `zfa>` Create fold in <> brackets

# Search and Replace
+ `/#` Find # searching forward
+ `?#` Find # searching backward
+ `n` Continue search downwards
+ `N` Continue search upwards
+ `%` Move to matching bracket from under cursor
+ `:s/old/new/g` Substitude old for new on line with no prompt
+ `:#,&s/old/new/g` Substitude old for new on lines # to & with no prompt
+ `:%s/old/new/g` Globally substitude old for new with no prompt
+ `:%s/old/new/gc` Globally substitude old for new with prompt

# External Calls
+ `:! <command>` Execute an external command in the shell
+ `:r <file>` Insert the contents of file at cursor position
+ `:r !<command>` Insert ouptut of command at cursor position

# Tabs
+ `:tabnew` Open a new tab
+ `:tabe <file>` Open file in a new tab
+ `<ctrl> PgUp` Switch to tab on Right
+ `<ctrl> PgDn` Switch to tab on Left
+ `:tabdo <command>` Run command in all tabs

#Panes
+ `:vnew` Split window/pane vertically
+ `:new` Split window/pane horizontally
+ `<ctrl> W + H` Switch to pane to the left
+ `<ctrl> W + L` Switch to pane to the right
+ `<ctrl> W + J` Switch to pane to the below
+ `<ctrl> W + K` Switch to pane to the above
+ `<ctrl> W + _` Give all vertical space to current pane
+ `<ctrl> W + |` Give all horizontal space to current pane
+ `<ctrl> W + =` Evenly distribute space for all panes
+ `<ctrl> W + +` Increase current pane height
+ `<ctrl> W + -` Descrease current pane height
+ `<ctrl> W + >` Increase current pane width
+ `<ctrl> W + <` Descrease current pane width

# File
+ `:e <file>` Open file
+ `:enew` New file
+ `:w` Save current file
+ `:w <file>` Save current file as filename
+ `:wq` Save and quit
+ `:x` Save and quit
+ `:q` Quit
+ `:q!` Force quit
+ `:bd` Delete/close buffer
+ `:hardcopy` Print file

# Location
+ `<crtl> G` Show current position in file
+ `:f` Show line numbers
+ `m[a-zA-Z]` Place mark [a-zA-Z] at cursor
+ `` `[a-zA-Z]`` Goto mark [a-zA-Z]
+ `:marks` Show all marks

# Text Insertion
+ `i` Insert text before cursor
+ `I` Insert text at beginning of line
+ `R` Start overtype mode
+ `a` Insert text after cursor
+ `A` Insert text af end of line
+ `o` Open new line following current line
+ `O` Open new line before current line
+ `v` Switch to visual selection mode
+ `V` Switch to visual line selection mode
+ `<crtl> v` Switch to visual block selection mode

# Movement
+ `h` Move cursor left
+ `l` Move cursor right
+ `j` Move cursor down
+ `k` Move cursor up
+ `gj` Move cursor down one display line
+ `gk` Move cursor up one display line
+ `H` Move cursor to top of display
+ `M` Move cursor to middle of display
+ `L` Move cursor to bottom of display
+ `w` Move cursor forward to start of next word
+ `e` Move cursor to end of next word
+ `b` Move cursor backward one word
+ `)` Move cursor forward one sentence
+ `(` Move cursor backward one sentence
+ `0` Move cursor to start of line
+ `^` Move cursor to first character of line
+ `$` Move cursor to end of line
+ `<ctrl> F` Move cursor forward one screenful
+ `<ctrl> B` Move cursor backward one screenful
+ `<ctrl> U` Move cursor up half a screenful
+ `<ctrl> D` Move cursor down half a screenful
+ `gg` Move cursor to top of file
+ `G` Move cursor to bottom of file
+ `#G` Move cursor to line #
+ `#gg` Move cursor to line #
+ `f#` Move cursor forward to next character # on line
+ `F#` Move cursor backwards character # on line
+ `t#` Move cursor forward to character before the next character # on line
+ `T#` Move cursor backward to character after the next character # on line

# Macros
+ `q[a-zA-Z0-9]` Start recording macro into register [a-zA-Z0-9]
+ `q` End recording of current macro
+ `@[a-zA-Z0-9]` Playback macro from register [a-zA-Z0-9]
+ `n@[a-zA-Z0-9]` Playback macro from register [a-zA-Z0-9] n times

#Misc
+ `u` Undo
+ `U` Restore line
+ `<ctrl> r` Redo
+ `J` Join line below to current line
+ `.` Repeat last command