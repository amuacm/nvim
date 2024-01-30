# Getting Started with Neovim

## Introduction

Neovim is a text editor that is designed as a fork of Vim, with the goal of improving the codebase, enhancing the user experience, and making it easier to implement plugins and APIs. It aims to be a more performant and maintainable alternative to Vim Neovim offers several advantages over Vim, including a more powerful plugin system, the ability to use the Lua programming language for plugin implementation, and compatibility with Vim plugins with minimal modifications. It also allows for remote procedure calls (RPCs) to extend the functionality of the editor asynchronously through any programming language. Neovim has gained popularity among developers due to its project maintenance, feature improvements, and the ability to write plugins in Lua. It is worth noting that while Neovim offers these advantages, Vim remains a popular and widely used text editor.

## Using Vim

Entering --INSERT-- mode can be achieved through: i (insert chr), a (append chr), I (insert line), A (append line).

## Motions

the basic motions in vim are `h`, `j`,`k`,`l` (left, down, right, up).

the next most basic and common are using `w` (word), `b` (back word), `e` (end word).
To move around on a line are commands like `^` (front line), `$` (end line), `%` (toggle brackets).

some advanced motions are `G` (top file), `g` (bottom file), `H` (top window), `L` (bottom window).

## Commands

the most basic commands are: `x` (delete chr), `r` (replace), `c` (change), `d`+motion (delete motion), `X` (backspace);
as well as: `u` (undo), `R` (redo), `y` (yank/copy), `p` (paste), `v` (select), `V` (select line).

a more confusing one that also comes in handy is `Ctrl+v` (visual block), which selects vertically over lines instead of on a single line. (use `I/A`, followed by `<Esc>` to add text to all selected files).

## combo moves

vim combines all these motions in a "{command, count} + motion" structure. 

for example: `d2w` -> 'delete 2 words'
             `dG` -> 'delete to end of file'
             `c$` -> 'change to end of line'
             `Vgg` -> 'select to top of file'
             `3yy` -> '3 line yank'

## :Ex commands

basic commands: `:w` (write/save file), `:q` (quit), `:wq` (write & quit).

another common command in to search and replace: `:s/old/new`
starting with `:%s` will apply the change to the whole file, wheras the regular `:s` will only be for the first instance of the change on a line or a selection.

add `/g` will make the change 'global' on a line, and adding 'c' will prompt the user to check for the instance.

finally `/` + any search term will show all instances of a search result, which can be cycled through with `n/N`.






