---
title: "Examples"
header:
  logo_header: /assets/images/core/logo_full_inverse.png
permalink: /docs-save-load-system/examples/
excerpt: "Examples."
last_modified_at: 2017-12-26T20:47:57-05:00
toc: true
---

Here are examples that may apply to your game requirements. Feel free to use them in your games :smile:

If you want to follow the next tutorials, please download the next link: [Project Example 4.16 Unfinished](https://www.dropbox.com/s/uym4k0soxlgoakl/AutoSaveLoadExample_TutorialPart04_4_16.zip?dl=0)

If you want a project example that has already all the tutorials completed, please download this link: [Project Example 4.18](https://www.dropbox.com/s/ev9rgckeshfgeso/CSWAutoSaveAndLoadExampleProject_v3_4.18.zip?dl=0)

This page will be updated with more examples in 4.19 (Async Save & Load and Cloud saving)
{: .notice--info}

## Destroy Runtime Generated Actors On Load

In this example i show you how you can setup the plugin so you only destroy runtime generated ```Actors``` if these weren't saved.
This is very useful as the plugin doesn't destroy unsaved ```Actors``` by default (because it could delete your level design work). 

You could be developing a game where you spawn ```Actors``` at runtime and you'll see that if you load your game, those ```Actors``` won't be deleted. Even if they weren't saved.
That may not be the behavior you're expecting so, in the next video, i show you how to solve this possible issue.

 <iframe width="560" height="315" src="https://www.youtube.com/embed/waSR2a4fyGc?rel=0&amp;showinfo=0" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

## Saving a Pickup and a Door State

This is a very simple example but it shows a good use case that could be applied to many games.

By saving and loading the Door state, i show you how this plugin can save and load a ```Timeline``` state. Saving the Pickup is more simple and straightforward.

<iframe width="560" height="315" src="https://www.youtube.com/embed/CreyTMUcuC0?rel=0&amp;showinfo=0" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

## Saving an AI Character State

An example about saving a simple AI that uses ```Behavior Trees```, ```Blackboard``` and ```AI Tasks```. In this example, the Load event can even restore the state of dead ```Characters```

<iframe width="560" height="315" src="https://www.youtube.com/embed/DTjYD4wc8bg?rel=0&amp;showinfo=0" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

## Saving the UMG State

In this example i show you how you can save your UMG state. As an example, we're going to save and restore the state of the ```Health```, ```Stamina``` and ```Score```.
This is done by storing those variables inside an ```Actor``` and using them to update the UI. In this case, the data is being stores in the ```ThirdPersonCharacter```.

<iframe width="560" height="315" src="https://www.youtube.com/embed/xPxkfIuQV7E?rel=0&amp;showinfo=0" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

In this video, new aux variables are created for solving issues while saving and loading certain ```Actors``` such as the door (```Saved```NamedVariables).
This is not neccesary now as the bug was solved for all versions of the plugin.
{: .notice--warning}

## Saving in Level Streaming and/or Multiple Levels.

In this example we're going to save ```Actors``` that will belong to diferent Levels/Sublevels.

If using Level Streaming, ```Actors``` can belong to the persistent level or any of its sublevels. ```Actors``` are saved taking into consideration to which levels they belong. 
The same thing happens when you load your game, only ```Actors``` for levels that are active will be loaded.

If using Multiple Levels, ```Actors``` are saved and loaded only for the current active level.

It's worth to mention that everything is saved in a single file but can be customized to be saved in separated files if needed. Also, ```Actors``` data that belong to inactive levels aren't erased when saving/loading the game.

<iframe width="560" height="315" src="https://www.youtube.com/embed/5SDihIet2gQ?rel=0&amp;showinfo=0" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

If using Level Streaming you may need to save/load only certain levels sometimes. The default functionality of the plugin is to always save/load all the levels that are active.
You can customize this functionality by using the "unfolded versions" of ```AutoFillSaveGameObject()``` and ```AutoLoadActorsData()``` which will allow you to filter which levels to save/load. 
For more information, see the Showcase Blueprint that comes in the Example Project.
{: .notice--info}

The new Async ```AutoFillSaveGameObject()``` and ```AutoLoadActorsData()``` functions that comes in the UE4 4.19 will allow to filter which levels will be saved and loaded by level name.
{: .notice--info}

## Extend/Convert the CSWAutoSaveGameObject

Here, we're going to extend the ```CSWAutoSaveGameObject``` in blueprints to customize it and save extra data. This is very useful as we can use this object to save "global data" as ```WorldScore```.
This is also useful for saving Blueprint Structures, we can create BP Structures inside the Save Object and use it to save & load them.

<iframe width="560" height="315" src="https://www.youtube.com/embed/Ufzc6zB4haA?rel=0&amp;showinfo=0" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

As of now, the component events such as ```OnSaveStart()``` and ```OnLoadEnd``` also retrieve the ```CSWAutoSaveGameObject``` reference that was used to save/load the game.
{: .notice--info}