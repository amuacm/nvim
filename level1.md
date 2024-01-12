# Configuring Neovim using VimScript

## step 1 | installing neovim

While using homebrew is recommended, neovim can easily be installed using apt:

` sudo apt install neovim `

## step 2 | Creating an init.vim file

Once neovim is installed, navigate to your .config folder in the home directory, and create a nvim folder if it does not already exist.

` mkdir ~/.config/nvim `

` cd ~/.config/nvim `

Now create and enter your init.vim file:

`nvim init.vim`

## step 3 | essential remaps and preferences

There are many different settings that can be added to neovim, here are a few essentals:

```
:set nu " add line numbers
:set rnu " line numbers based on distance from cursor, helpful for switching between lines quickly
:set mouse=a " enable mouse

vnoremap J ":m '>+1<CR>gv=gv" " These remaps allow you to move selected text easily
vnoremap K ":m '>+1<CR>gv=gv"
```

## step 4 | installing a plugin manager

## step 5 | essential plugins


