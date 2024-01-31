# Configuring Neovim using VimScript
## step 1 | installing neovim

While using homebrew is recommended, neovim can easily be installed using apt:

` sudo apt install neovim `

## step 2 | Creating an init.vim file

Once neovim is installed, navigate to your .config folder in the home directory, and create a nvim folder if it does not already exist.

 ```
 mkdir ~/.config/nvim
 cd ~/.config/nvim
 ```

Now create and enter your init.vim file:

`nvim init.vim`

## step 3 | essential remaps and preferences

There are many different settings that can be added to neovim, here are a few essentals:

```
:set nu " add line numbers
:set rnu " line numbers based on distance from cursor, helpful for switching between lines quickly
:set autoindent
:set mouse=a " enable mouse

vnoremap K :m '>+1<CR>gv=gv " These remaps allow you to move selected text easily
vnoremap J :m '>-2<CR>gv=gv

inoremap <C-c> <Esc> " it's just easier than hitting escape
inoremap kj <Esc> " even faster!

inoremap ; : " blazingly fast
```

## step 4 | installing a plugin manager

Plugin Managers are useful for adding extra upgrades to nvim to improve the user experience.
A simple plugin manager is vim-plug which can be installed like this:

*you may need to install curl before running this command*

```
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

**NOTE: Only use this command if you are using neovim, vim requires a different command, which can be found at the vim-plug repository: https://github.com/junegunn/vim-plug** 

## step 5 | essential plugins

After installing vim-plug, return to your init.vim file, and add the following code:

```
call plug#begin('~/.config/nvim/plugged')

Plug 'https://github.com/vim-airline/vim-airline' " Status bar
Plug 'https://github.com/preservim/nerdtree' " NerdTree
Plug 'https://github.com/ryanoasis/vim-devicons' " Developer Icons
Plug 'https://github.com/rafi/awesome-vim-colorschemes' " Retro Scheme
Plug 'https://github.com/jiangmiao/auto-pairs' " bracket completion
Plug 'http://github.com/tpope/vim-surround' " Surrounding ysw)
Plug 'https://github.com/ribru17/bamboo.nvim' " special colorscheme 
Plug 'http://github.com/alvan/vim-closetag' " HTML tag completion

set encoding=UTF-8

call plug#end()

nnoremap <C-f> :NERDTreeToggle<CR> " remap to use NERDTree
```

Next, save the file and install the plugins by typing `:PlugInstall` followed by the command `:so` to source the file.
Your plugins should all update from here.

## step 6 | using lsp with conqueror of combinations

### install coc plugin

First, add the following repository to your init.vim file:

```
Plug 'https://github.com/neoclide/coc.nvim'
```
be sure to `:PlugInstall` to load the plugin.

### installing node dependencies

install these node dependencies to allow the coc to run properly. 
NOTE: if you are on macOS, replace apt with port.

```
sudo apt/brew install nodejs
```

```
sudo apt/brew install npm
```

### building with yarn

Now, change directories and install yarn:

```
cd plugged/coc.nvim
sudo npm install -g yarn
```

Once installed, enter the following command:
```
yarn install
```
followed by:
```
yarn build
```

### installing completion support
Now, to add completion for a particular language, open a file of that type using nvim, and enter the following command into the nvim terminal (python can be replaced with any language in that format):

```
:CocInstall coc-python
```

### installing a language server
To install a language server, you will need to use pip, a package management system for python.

```
sudo apt install python3-pip
```

Finally, return to the terminal and install the particular language server for the language. python uses the jedi-language-server, so we will install that here:

```
pip3 install jedi
```

You should now have code completion added to your python files.







