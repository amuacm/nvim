# Getting Started with Neovim

## Introduction

Neovim is a text editor that is designed as a fork of Vim, with the goal of improving the codebase, enhancing the user experience, and making it easier to implement plugins and APIs. It aims to be a more performant and maintainable alternative to Vim Neovim offers several advantages over Vim, including a more powerful plugin system, the ability to use the Lua programming language for plugin implementation, and compatibility with Vim plugins with minimal modifications. It also allows for remote procedure calls (RPCs) to extend the functionality of the editor asynchronously through any programming language. Neovim has gained popularity among developers due to its project maintenance, feature improvements, and the ability to write plugins in Lua. It is worth noting that while Neovim offers these advantages, Vim remains a popular and widely used text editor.

## Installing Neovim using Homebrew

This tutorial assumes that users are using either Linux/WSL or MacOS to install nvim.

While using apt to install nvim is sufficient, in order to get the most recent updated and the ability to use Lua (explained later), it is necessary to use an additional plugin manager. For this tutorial, we can use homebrew.

### Installing Homebrew
(Find more information at https://brew.sh/)

Open up a terminal and type in the following command:

` /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" `

Once completed, homebrew will ask you to make a few changes in their "Next Steps" section. Please complete these before continuing.

### Installing Neovim

Now that Homebrew is installed, simply type the following command into the termianal:

` brew install neovim `

Once completed, you should be able to open vim by typing 'nvim' into the terminal.

## Next Actions

### Creating Neovim configuration folder

Before adding more customization into vim, you will need to create a specific folder neovim to find your settings.

Type the following command into the terminal:

` mkdir ~/.config/nvim `

### Customization

This tutorial will offer to tracks to customize nvim. The first and more simple option is to use Vimscript, the second is to use lua. Both are embedded into vim and will require no other installations beyond plugins. the Vimscipt is simpler, but lua is objectively more powerful and faster. Choose based off your interest and skill level.
