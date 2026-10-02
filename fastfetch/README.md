# Fastfetch

Fastfetch is a command tool that get you information about your PC  in the terminal

Here's a custom one i made for the club of my school, [Robotech](https://github.com/Robotech-Lillois).

![img]()

# Installation

First of all, you need to have to install fastfetch, here's how :

```bash
sudo apt install fastfetch #On debian
sudo pacman -S fastfetch   #On arch
```

Then you want put the config files in the `.config/fastfetch` folder of your home directory :

```bash
# clone the repo
git clone https://github.com/Gaettan-Git/dotfiles.git 

# if needed, you can create the folder for fastfetch config
mkdir .config/fastfetch

# then move the config files to fastfetch
cp -r dotfiles/fastfetch .config/fastfetch
```

You can now type `fastfetch` in your terminal, and enjoy !
