# GameOn
GameOn is an Open Source solution to playing Unity3D games outside the browser, with a-click, and still keeping the ```.unity3d``` file hosted on developer's server. Perfect for indie developers and game portals. 

Install [GameOn from Releases](https://github.com/chall3ng3r/GameOn/blob/master/Releases/GameOn_0_9_setup.zip?raw=true) folder, and [try demoes here](https://dl.dropboxusercontent.com/u/175621/GameOn/game-demos.html)

Currently its only for Windows, and I am planning for MacOS and Linux versions with help from Unity3D developer community. If you want to contribute, you're most welcome :)

# How It Works?
The solution is that end-user install this tiny GameOn application on PC, the concept is just like Steam. This application will handle the click from browser and start the game outside the browser, in new window.

![GomeOn](https://github.com/chall3ng3r/GameOn/blob/master/Media/GameOn-demo.gif?raw=true)

Installing GameOn is one-time process, afterwards users can just click on websites which have GameOn enabled links to start playing games. 

GameOn resigters itself as ```gameon://``` URL scheme handler when installed. There's also a wrapper Windows application which is launched when user clicks GameOn enabled links. This application just holds Unity Web Player ActiveX control, and parses the clicked URL, formats it, and passes it on to Unity Web Player. 

# What's New
Version 0.9.2048
- pass "size=width,height" in URL to set window size
- proper handling of URL
- updated binary release
- cleaned unused references
- installer script updated
- demo HTML page updated with link samples

# For Developers
Adding GameOn to your website or portal is pretty simple.

Before you made link to a page with embeded Unity Web Player like:
```
<a href="http://website.com/game_demo.html">Play Game</a>
```
For GameOn, you simply make links like:
```
<a href="gameon://website.com/game_demo.unity3d?size=800,600">Play Game</a>
```

Important things to note:
- Always use absolute URL to your ```.unity3d``` file, replacing ```http://``` with ```gameon://```
- Pass ```size=width,height``` as querysting with the URL, for player window size. Default is 640x480

That's it!

P.S. as this is the first release, few things are not yet final, like icon and URL parameters for window size.

# Contribute
GameOn is developed with Visual Studio 2015 Community edition. Use the same version to open and work with this project.

The installer is made with NSIS, and script is in Installer folder.
