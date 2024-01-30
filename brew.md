# Installing Neovim using Homebrew

This tutorial assumes that users are using either Linux/WSL or MacOS to install nvim.

While using apt to install nvim is sufficient, in order to get the most recent updated and the ability to use Lua (explained later), it is necessary to use an additional plugin manager. For this tutorial, we can use homebrew.

## Installing Homebrew
(Find more information at https://brew.sh/)

Open up a terminal and type in the following command:

` /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" `

Once completed, homebrew will ask you to make a few changes in their "Next Steps" section. Please complete these before continuing.

## Installing Neovim

Now that Homebrew is installed, simply type the following command into the termianal:

` brew install neovim `

Once completed, you should be able to open the application by typing 'nvim' into the terminal.


