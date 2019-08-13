<img src="https://electronjs.org/app-img/android-messages/android-messages-icon-128.png">

# Android Messages

A clean and native interface to https://messages.google.com/web. Supports dark and light mode on macOS Mojave. This project is 100% open-source and available for macOS. Enjoy!

![Android Messages](https://i.imgur.com/O3H5NWh.png)

![Android Messages](https://i.imgur.com/UUsxiqv.png)

## Build Instructions

To build a new version of the application,  first download [nativefier](https://www.npmjs.com/package/nativefier) using the following command:

```
yarn global add nativefier
```

**OR**

```
npm install nativefier -g
```

Next, download the required CSS and image assets from one of the releases here located [here](https://github.com/nparsons08/android-messages/releases). For example, you will need the [electron.css](https://github.com/nparsons08/android-messages/releases/download/v1.0.0/electron.css) and [logo.png](https://github.com/nparsons08/android-messages/releases/download/v1.0.0/logo.png) files.

Last, you'll need to run the `nativefier` command to build your package.

```
nativefier --name "Android Messages" --platform "osx" --bounce --counter  --honest --hide-window-frame --disable-dev-tools --title-bar-style "hidden" --icon logo.png --inject electron.css "https://messages.google.com/web"
```

> Note: Nativefier allows for `osx`, `mas`, `linux`, and `windows` platform types. You can specify this with the `--platform` flag.

