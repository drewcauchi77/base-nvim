# How To Setup this NVIM configuration (Windows)

## Supports (Linters and Formatters)

My Neovim supports:
1. C# (C-sharp)
2. Lua 
3. Javascript (needs revisions)
4. Python (needs revisions)

## Steps

1. Make sure to have Chocolatey installed - if not install it from https://chocolatey.org/install 
2. After the installation is complete, open Powershell with admin rights.
3. Run ``choco install neovim``.
4. Wait for the installation to complete and run ``cd $env:LOCALAPPDATA``.
5. This will take you to the local data folder of Windows.
6. Create a new folder called nvim and enter it by running ``mkdir nvim & cd nvim``.
7. Clone the repository by running ``git clone https://github.com/drewcauchi77/base-nvim.git .``.
8. Run ``nvim`` in that same directory.
9. Neovim will open and lazy will start installing packages.

At this point, you already have a working Neovim installation and you can start coding and adding stuff to it. However, in the base file I have added some things that require some other things that you would need to setup to make sure you have the best Neovim experience!

## Fonts

My base setup includes a dependency called ``nvim-web-devicons``. On Windows, you need to download these icons/font file and make sure that the terminal's default font is set to this icons/font file.

1. Go to https://www.nerdfonts.com/font-downloads and find a font that you like. I am using LiterationMono Nerd Font (looks like this: https://www.programmingfonts.org/#liberation)
2. Download the font package from the NerdFonts site.
3. Extract the .zip folder that you download and install the .ttf font that you would like.
4. Once the font is installed, go to your terminal and right-click the top bar. Go to Settings.
5. This will open a new tab in your terminal where you can select the default terminal settings.
6. From the left hand side panel, go to Defaults > Additional Settings > Appearance.
7. In the Text section, you will find Font face. From there select the font that you have installed (in my case LiterationMono Nerd Font).
8. Close and re-open the terminal and run ``nvim``.
9. You should now be met with icons in your home screen. These icons will also be shown in the left-side panel for files, errors, git messages etc..

## C# Setup

You need to make sure that you have the Dotnet SDK installed. Honestly, I cannot be 100% whether there are any complications to run this or not but I'm guessing you need to do so from here: https://dotnet.microsoft.com/en-us/download. My Dotnet SDK solution was installed automatically when I installed Visual Studio 2022 for my C# projects.

## Lua Setup

Lua is the main language for the Nvim setup and is an increasingly favourite language for myself. There are some additional steps to make sure that the proper Lua linter and formatter is installed on Windows.

1. Open nvim and run ``:Mason``
2. Check the package version of ``lua-language-server``. Mine is 3.13.3.
3. Download Lua as a .zip from the following  link: https://github.com/LuaLS/lua-language-server/releases/tag/3.13.3
4. Run ``cd $env:LOCALAPPDATA`` and create a bin directory by ``mkdir bin``.
5. Inside the bin directory, create another folder called lua-language-server: ``cd bin`` followed by ``mkdir lua-language-server``.
6. Move all the extracted contents from step 3 top this new directory.
7. Once moved, in your Windows start menu look for Environment Variables.
8. In the User Variables section, select Path and press Edit.
9. Press on New and add the following path: ``%LOCALAPPDATA%\bin\lua-language-server\bin``.
10. Make sure to Save the changes.
