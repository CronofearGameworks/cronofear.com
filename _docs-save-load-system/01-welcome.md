---
title: "Welcome"
header:
  logo_header: /assets/images/core/logo_full_inverse.png
permalink: /docs-save-load-system/welcome/
excerpt: "Welcome."
last_modified_at: 2017-12-26T09:49:52-05:00
toc: true
---

Hi!, welcome to the documentation of the "CSW Autosave and Load System w/compression" plugin for Unreal Engine 4. If you want to purchase the plugin, 
see the description page or download the project example, please refer to: [Marketplace Link](https://www.unrealengine.com/marketplace/csw-autosave-and-load-system-w-compression)

## About the plugin

This product is a C++ plugin for Unreal Engine 4. Although the plugin is written in C++ all the functionality **can be used in Blueprints very easily**. This plugin is mainly aimed to indie solo or team developers 
but it can be easily escalated to bigger projects due to its async save and load support(since 4.19). Even more considering that the source code is accessible and well commented.

The plugin is developed with a "generic-programming pattern" in mind, in a way that it can be used in all kind of project. It's so flexible in fact, that it can even used for features that weren't considered beforehand. 
As an example of the flexibility of this plugin, you can check: [Undo/Redo System](https://www.youtube.com/watch?v=7HyOPZ2ZlRY) and [Cloud Save](TODO).

Of course, the main goal of the plugin is to **simplify the implementation of a Save and Load system in your game**. To achieve that, the plug-in is very straight forward in the way it works and it's easy to understand. 
In fact, if you already have implemented a save and load system using the built-in features from Unreal Engine before, you'll see that this plugin is not very different. 
Actually, this **plugin extends from the Unreal Engine features** so you can still use the logic you've implemented (SaveGameToSlot(), LoadGameFromSlot(), change the parent of your Save Game Object, etc.).

If you haven't yet implemented a Save and Load system in your game, fear not! **This documentation is aimed for beginners and advanced users** (for advanced users, mainly the customization part). 
If you have problems following the documentation, i have also created some nice video tutorials: [Videotutorials](https://www.youtube.com/watch?v=IMySm5q617o&index=2&list=PL7Se41ZzAKZmPVJGCaFxv1bPMXqPgEOQa) which i hope you'll find useful.

## Why buy this plugin?

I know, if you're here then you probably already bought the plugin. But one can never know. If you're wondering why would you buy this plugin in the first place then i have a very nice list or reasons right here:

* Much of the save and load work is done behind the scenes. **You don't have to worry about the complexity of a save system** but only about how you want to implement the system in your game. 
Not all the games use the same save and load system but this plugin is designed in a way that can be adapted to pretty much any game!
* **Very easy to use.** You add a component to the Actors you want to save, call the saving functions when you want, call the load functions when you want and that's it! At least the basic functionality. 
The plugin even auto handle for you the Transforms and the Physics simulation states of your Actors (position, rotation and velocity) so you don't have to worry about that. 
Of course, you can disable this auto-functionality any time for any Actor, even in runtime.
* **Customizable component.** If you attach my component to an Actor, you'll be able to customize (even in runtime) the way this Actor will be saved and loaded. 
By default you can save even the components and child Actor components from the Actor or you can set which components you want or you don't want to be saved.
* **Save Variables in a breeze**. Even for components. You only have to check a property for the variables you want to save, it's that easy.
* **Async Save & Load Support.** Since 4.19, now you don't have to worry about hiccups in your game when saving and loading.
* Fast! The plugin is written in C++ so it's really fast.
* **It has compression feature.** This will allow you to keep your save files very small in size. Why would you want that? For implementing a cloud save and load system for example! 
You can convert your save object into a compressd String and send it to a cloud provider, [like this](TODO). 
This plugin is so nice in fact, that can convert ANY object into a compressed string so you can actually send almost any UE4 data to the Internet.

## **About this documentation**

As of December 2017, this documentation is not yet finished. Some links may refer to "**/TODO**" which means that will be updated.
{: .notice--info}