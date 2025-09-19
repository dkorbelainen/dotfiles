-----

# dotfiles

This repository contains my personal dotfiles for **EndeavourOS** with the **KDE Plasma** desktop environment.

-----

### Installation

1.  **Clone the repository:**

    ```sh
    $ git clone git@github.com:DanielKorbelainen/dotfiles.git
    $ cd dotfiles
    ```

2.  **Use GNU Stow to create symlinks:**

    ```sh
    $ stow .
    ```

-----

### Structure

My dotfiles include configurations for the following applications:

  * **Zsh**: Shell configuration.
  * **Ghostty**: Terminal emulator.
  * **KDE Plasma**: Theme, panel, and window manager settings.
  * **Fastfetch**: System information utility.
  * **Flameshot**: Screenshot tool.
  * **Micro**: Terminal-based text editor.
  * **Ulauncher**: Application launcher.
  * **Wallpaper**: My wallpaper is included in the `assets/` directory.

### Notes

  - To use the wallpaper included in this repository, copy the image to your `~/Pictures` directory.
  - After running the `stow` command, you may need to **log out and log back in** to see the changes.
