unity-ios-plugins
=================


(project finally migrated from bitbucket to github for posterity/entertainment)


What is this?
-------------
Just a couple plugins I wrote or forked and used in my Unity projects.  These will only be useful to you if you are making an iOS game in [Unity](http://unity3d.com/).


Installation
------------
If you don't already have a ```Plugins/``` folder in your project, create on and drop all the files in there.  Your structure should look like this:
--Assets/
----Plugins/
------<all C# plugin files go here...these are what talk to/interface the native iOS implementation files>
------iOS/
--------<all iOS implementation files go here...these are the native Objective-C files that can use the Cocoa framework>


After you have done this, and the time comes to build to device, you will need to add the ```Twitter.framework``` to your frameworks (Build Phases --> Link Binary With Libraries).
This probably can and should be automated if you know about Unity/iOS post processor stuff, but I am not knowledgeable about that yet.


Alert View Usage Example
------------------------
In any script file:
```AlertViewPlugin.ShowMessage("test title", "wo0t!  This is a normal alert view working in unity!");```
(of course, you need to build to device to test...nothing happens if you test on Desktop)


Twitter Usage Example
------------------------
In any script file:
```TwitterPlugin.ComposeTweetWithScreenshot("I scored 5000 points!  Beat that!", "http://somelinkhere.com");```
(of course, you need to build to device to test...nothing happens if you test on Desktop)
*NOTE - You need to add the twitter.framework in your iOS XCode project or it will not even compile.


Attribution
-----------
The twitter plugin was originally borrowed from [Keijiro-san's unity-ios-twitter plugin](https://github.com/keijiro/unity-ios-twitter) in an attempt to improve the documentation/usage.  Looking back though, I didn't really do anything and just showed usage here instead :/
