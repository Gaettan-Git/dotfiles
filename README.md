<h1 align="center">Plymouth oiiaa cat</h1>
The greatest boot animation in history

---

# About this repo

I basically took exemple of [This repo](https://github.com/adi1090x/plymouth-themes). I copy one of theme and replace the animation by this magificent cat.<br>
---

# How to install

+ Here's how you can do it on a debian distro

First make sure plymouth is installed (should be) :

```bash
sudo apt install plymouth
```

Then you want to get the file of this theme on your plymouth folder :

```bash
# Copy this repo on your computer.
git clone https://github.com/Gaettan-Git/plymouth-oiiaa

# you go to the repo files
cd plymouth-oiiaa

# you copy the theme folder, containing the script and images, in your plymouth themes
sudo cp oiiaa /usr/share/plymouth/themes
```

Then we have to make plymouth recognize this theme :
