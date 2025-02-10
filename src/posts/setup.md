---
date: 2025-02-10
title: A Distraction-free Setup
description: throw away your tv
tags:
  - post
---
## Distractions are the enemy
A computer's primary purpose is to ease the creation, storage, and transmission of information. Any other functionalities are distractions from this core purpose.
Applications like video games, media playback, and social networking have emerged as distractions that divert attention away from a computer’s intended purpose.

I do believe that there is a place for computers to be entertainment machines.
But entertainment machines and productive machines must not combined together as one.
When I perform productive activities, the availability of entertainment alone is enough to distract me from the work.
I usually don't have enough brain power to resist the temptation of entertainment, and relying on willpower everytime I open a computer to work is not sustainable.

When making productivity the only function available in a computer, I begin to treat it like how it's supposed to be, a tool.
I open the computer when and only when I do my work.
When using the work computer, I cannot do anything else outside of working on that computer.
Work is the only thing I do on the computer not because I extract alot of willpower to do it, but because the computer doesn't have the distracting functionalities that pull me away from work.

## The sword
To support this idea, I’ve designed a setup dedicated only to document creation.
This is the most minimal setup for text creation that I can come up with.
Removing further the features of this setup will sacrifice aesthetic and convenieces.

### Kien's Text Creating Machine:
Begin with a fresh Arch installation, either using the manual method or the archinstall script, then install:

#### Display server (Xorg)
A display server is installed to allow graphical programs such as window managers and browsers to be displayed. Xorg can be installed as an option in the archinstall script.

#### Window manager (dwm)
A window manager organizes your working windows and allow you to have multiple work spaces. With window managers, you can have dedicated worspaces for each of your work tasks. For example, in my setup, I have one workspace dedicated for text editing, and another workspace to display the rendered text document.

#### Terminal Emulator (st)
A terminal emulator is installed to extend the capability of your termial UIs. With it, you can add into your terminal functions such as copy and paste from clipboard, scroll backs, color schemes or font resize. A note here is that you will usually have a narrower color scheme options in your text editor if you don't use a terminal emulator that allows a wider range of colors.

#### File manager (lf or ranger)
To quickly navigate and preview your files. You can integrate images and document displayer into your file manager to preview files in your file manager. I reccomend ```feh``` for image displaying and ```zathura``` for document displaying.

#### Text editor (neovim)
A text editor is your main program to create and edit your documents in. Through different text editors, you will have different shortcuts and bindings to navigate and edit your documents. I recommend nano as an easy-to-use text editor that requires no prior learning to get started. However, nano becomes limiting quickly, that's when I urge you to learn how to use Vim. Vim bindings will forever change the way you type, and it's worth every second to learn it. This is not an article about Vim, but I'm allowing this section about Vim to be long to emphasise how much Vim bindings will make your text editing time more efficient and pleasant.

I use neovim, and extended version of vim, which allows me to install unique plugins that I find useful. Start with [kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim), then install:
- A clipboard copy backend (I installed ```xclip``` with pacman)
- A different color scheme. I settled with ```onedark```, a black color scheme to not get distracted by colors.
- Tab complete. Enable it at the  ```nvim.cmp``` section in ```init.rc```
- Auto closing brackets (nvim)
- Project view bindings with ```vim.keymap``` ```vim.cmd.Ex```
- Add language servers with ```:Mason```
- Relative line numbers

#### Browser (firefox)
Depending on the type of document you're creating, you may or may not need a browser on your machine. Keep in mind that browsers can be a gateway for distractions to pour in. Firefox is the easiest browser to install, I got it through pacman.

## Who is this setup for
This setup is suitable for any types of text editing. Depending on your work, you would want to extend this setup with programs from your field of work, for example, Latex for complex document formatings, or compilers and git if you program software. If .docx or pdf is your primary document type, I reccommend writing and editing in Latex and export it into .docx/pdf with ```pandoc```. Spreadsheets can be done on the terminal UI too, with ```sc``` or ```oleo```.

The main feature of this setup is that it’s built from a bare minimal operating system with no unnecessary applications. With only the essential programs for your work, distractions are nonexistent, leaving you with no choice but to focus or step away from the machine. A designated space to work is what this setup offers, and focus is what it will delivers. This setup embraces the "one device one job" philosophy, seperating the proverbial "TV" from the "textbooks".
