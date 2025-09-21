# dotfiles

This repository contains my personal dotfiles for arch-based [EndeavourOS](https://endeavouros.com/) with the [KDE Plasma](https://kde.org/plasma-desktop) desktop environment.

My goal was to create a fresh, ready-to-use setup by including as many KDE and application settings as possible. However, due to the personal nature of some configurations, you may still need to adjust a few things to perfectly suit your needs.

-----

### Requirements

Before proceeding, make sure you have the necessary packages and tools installed.

```sh
# Install core packages from official repositories
sudo pacman -S git stow ghostty fastfetch flameshot micro zsh wl-clipboard inter-font

# Install Ulauncher from the AUR
git clone https://aur.archlinux.org/ulauncher.git
cd ulauncher
makepkg -is
cd ..
```

  * **Change your default shell to Zsh:**
    ```sh
    chsh -s $(which zsh)
    ```

Reboot.

-----

### Installation

1.  **Clone the repository:**

    ```sh
    git clone https://github.com/DanielKorbelainen/dotfiles.git
    cd dotfiles
    ```

2.  **Use GNU Stow to create symlinks:**

    ```sh
    stow . --adopt
    ```

**Note on Stow:** The `--adopt` flag allows Stow to take control of existing configuration files and move them into this repository. It's an effective way to manage your current setup. However, in rare cases, if a file or directory is in the way, Stow may fail. If this happens, you will need to manually remove or rename the conflicting item (e.g., `mv ~/.config/conflicting_file ~/.config/conflicting_file.bak`) and re-run the `stow` command.

**Note on Autostart:** After installation, you must go into **System Settings \> Startup and Shutdown \> Autostart** to manually add applications like Ulauncher and Flameshot so they start automatically with your system.

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

  * To use the wallpaper included in this repository, copy the image to your `~/Pictures` directory.
  * After running the `stow` command, you may need to **reboot** to see the changes.
  * I also like to set up other tools such as **WireGuard**, **Obsidian**, various **IDEs**, **Firefox**, and my **DAW** depending on my needs.
