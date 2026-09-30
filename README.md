<h1 align="center">Plymouth oiiaa cat</h1>
The greatest boot animation in history. May solve world peace.<br>

![gif](https://github.com/Gaettan-Git/plymouth-oiiaa/blob/main/presentation_suggestion.GIF)

# About this repo

I basically took exemple of [This repo](https://github.com/adi1090x/plymouth-themes). I copy one of theme and replace the animation by this magificent cat.<br>

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

Then we have to make plymouth use this theme :

```bash
# Here's how to change plymouth default
sudo plymouth-set-default-theme oiiaa

# you can preview the theme by taping the following 
sudo plymouthd; sudo plymouth --show-splash; sleep 5; sudo plymouth --quit
# It show the current theme selected for 5 seconds

# and now you update the booting process
sudo update-initramfs -u
```

If everything worked correctly, you now have a spinning cat to greet you !!

# How to add your distro logo

In a future update (don't ask how future it'll be), i will try to make the animation recognize your distribution, and change the logo accordingly.<br>
For now, if you want it to show up, you have to add it "manually".

1. Download your distro logo from the internet (or anything, i won't check)
2. Add the following code in the end of the `oiiaa.script` file :

```bash
# display logo
distro_image = Image("Your logo filename"); # change filename accordingly
distro_sprite = Sprite();

distro_sprite.SetImage(distro_image);
distro_sprite.SetX(Window.GetX() + (Window.GetWidth() / 2 - distro_image.GetWidth() / 2)); # center the image horizontally
distro_sprite.SetY(Window.GetHeight() - distro_image.GetHeight() - 250); # display just above the bottom of the screen
```

If you add the logo, i recommand to get the cat to display just a bit higher, by diminuiting his y coordinate, line 37 of `oiiaa.script`<br>
> flyingman_sprite.SetY(Window.GetY() + (Window.GetHeight(0) / 2 - flyingman_image[0].GetHeight() / 2) - 150); for 150 pixels up
