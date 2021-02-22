# My build of ST v0.8.4

![](https://hostr.co/file/obSXadt8ekL0/st.png)

This repository hosts the source code of my build of ST (Simple Terminal) from the [Suckless software](https://st.suckless.org/). It is based on ST v0.8.4 and different patches have been applied in order to provide the features I liked. The list applied patches can be found in the *patches* folder. It features the following settings:

* Truecolor terminal with 256 colors supported (built-in)
* If *fontconfig* is installed, antialiased fonts are supported (built-in)
* Transparent background if configured
* Bold texts are not rendered using the bright variant of the current color
* Ability to configure multiple fonts (useful when main font cannot render certain characters)
* Full ligature support
* Built-in scrollback
* Vertically center lines in the available space
* Allows to launch an instance of ST in a specific directory (with the *-d* flag)

# Dependencies
The following packages are necessary in order to run this build of DWM properly:

* ttf-jetbrains-mono
* ttf-joypixels

Used fonts can obviously be modified in the *config.def.h* file if you don't want to use the two mentioned above.

# Installation
Basically, just clone this repository (or download it), compile the build and install it. Type the following commands:

```
git clone --depth 1 https://github.com/GSquad934/st.git
cd st
sudo make clean install
```

This build of ST integrates nicely with [my custom build of DWM](https://github.com/GSquad934/dwm).

# Running ST
ST can be run simply with the *st* command. It has a number of flags available:

```
usage: st [-aiv] [-c class] [-d path] [-f font] [-g geometry] [-n name] [-o file]
          [-T title] [-t title] [-w windowid] [[-e] command [args ...]]
```

Each flag (except for *-d* which is explained above) is detailed in the ST [manpage](https://www.mankier.com/1/st).

# Contact
You can always reach out to me:

* [Twitter](https://twitter.com/gaetanict)
* [Email](mailto:gaetan@ictpourtous.com)
