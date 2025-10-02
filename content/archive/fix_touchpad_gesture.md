+++
date = '2025-10-02T03:51:22+05:30'
title = 'How to fix touchpad gestures on Ubuntu'
tags = ['linux', 'guide']
+++

## Install and enable Touchegg

{{<linkicon "https://github.com/JoseExposito/touchegg" "fa-brands fa-github" "Touchegg">}} is a daemon that transform the gestures you make on your touchpad or touchscreen into visible actions in your desktop.

If you are using Ubuntu or Debian, use the following commands to install it from the official PPA:

```sh
sudo add-apt-repository ppa:touchegg/stable
sudo apt update
sudo apt install touchegg
```
> Instructs for other distributions available at {{<linkicon "https://github.com/JoseExposito/touchegg" "fa-brands fa-github" "Touchegg Github Repository">}} 

Once installed, you should start the daemon:
```sh
sudo systemctl start touchegg
```

You should also make it start automatically at each boot:

```sh
sudo systemctl enable touchegg.service
```

With that done, you should go ahead and install the X11 Gestures extension.

## Install and enable X11 Gestures GNOME extension

Go to the extension page and enable it: {{<linkicon "https://extensions.gnome.org/extension/4033/x11-gestures/?ref=itsfoss.com" "fa-solid fa-globe" "X11 Gestures Extension">}}

![X11 Gestures gnome extension](https://itsfoss.com/content/images/wordpress/2021/07/x11-gestures-gnome-extension-800x248.png)

Once you have enabled it, you can test the three finger swipe immediately. No need to log out or restart.

> For more in depth review, Read the original article at {{<linkicon "https://itsfoss.com/three-finger-swipe-gnome/" "fa-solid fa-blog" "It's Foss">}}
