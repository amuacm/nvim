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

vnoremap K ":m '>+1<CR>gv=gv" " These remaps allow you to move selected text easily
vnoremap J ":m '>-2<CR>gv=gv"

inoremap <C-c> <Esc> " it's just easier than hitting escape
```

## step 4 | installing a plugin manager

Plugin Managers are useful for adding extra upgrades to nvim to improve the user experience.
A simple plugin manager is vim plug which can be installed like this:

```
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

**NOTE: Only use this command if you are using neovim, vim requires a different command, which can be found at the vim-plug repository: https://github.com/junegunn/vim-plug** 

## step 5 | essential plugins

After installing vim-plug, return to your init.vim file, and add the following code:

```
call plug#begin()

Plug 'https://github.com/preservim/nerdtree' " NerdTree
Plug 'https://github.com/vim-airline/vim-airline' " Status bar
Plug 'https://github.com/ryanoasis/vim-devicons' " Developer Icons
Plug 'https://github.com/rafi/awesome-vim-colorschemes' " Retro Scheme
Plug 'http://github.com/tpope/vim-surround' " Surrounding ysw)
Plug 'https://github.com/ribru17/bamboo.nvim' " special colorscheme 
Plug 'https://github.com/jiangmiao/auto-pairs' " bracket completion
Plug 'http://github.com/alvan/vim-closetag' " HTML tag completion

set encoding=UTF-8

call plug#end()

:colorscheme bamboo " set colorscheme

nnoremap <C-f> :NERDTreeToggle<CR> " remap to use NERDTree
```

Next, save the file and intall the plugins by typing `:PlugInstall` followed by the command `:so` to source the file.
Your plugins should all update from here.

## step 6 | using lsp with coqueror of combinations
