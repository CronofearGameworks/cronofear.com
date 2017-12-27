---
title: "Quickstart Guide"
header:
  logo_header: /assets/images/core/logo_full_inverse.png
permalink: /docs-save-load-system/quick-start-guide/
excerpt: "Quickstart Guide."
last_modified_at: 2017-12-26T22:39:43-04:00
toc: true
---

## Enabling the Plugin.

Here, i show you how to enable the Plugin in your project. Once enabled you can use the functionality this plugin provides.

<iframe width="560" height="315" src="https://www.youtube.com/embed/IMySm5q617o?rel=0&amp;showinfo=0&amp;start=01&amp;end=44" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

This tutorial is using the ThirdPerson Template.
{: .notice--info}

## Creating the global Save & Load Functions

You need to call the global Save and Load functions from somewhere. In this example i show you how you can do that from a ```Player Controller```. You can actually place these functions in any ```Actor``` you want depending on your project needs :smile:.

<iframe width="560" height="315" src="https://www.youtube.com/embed/IMySm5q617o?rel=0&amp;showinfo=0&amp;start=49&amp;end=392" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

In newer version "CGD" prefixes has been changed to "CSW".
{: .notice--info}

## Saving and Loading an Actor

Here, i show you a simple example about creating an ```Actor```, adding the ```CSWAutoSaveComponent``` and Saving it and loading it from Disk/Memory by using the global Save & Load Functions we created before.
Very easy and straigthforward!

<iframe width="560" height="315" src="https://www.youtube.com/embed/IMySm5q617o?rel=0&amp;showinfo=0&amp;start=393" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

The delay() node added in the minute **9:00** is only waiting one frame and it's neccesary if you want to load your game exactly on BeginPlay().
{: .notice--info}

## Customizing the Save and Load Functionality

Here i show you how to customize the functionality of the Save & Load system. You can save custom variables just by checking a property.

As an example, in the video, we're going to save and load a ```CharacterMovementComponent``` state (```isFalling``` and ```velocity```).

Also, i'll show you an alternative method to save variables (using ```GetSavedVariables()``` and ```SetSavedVariables()```).

Finally, the video also shows you how to save Actor Components *"on demand"*. An ```Actor``` can be customized to save only the components you want to save!

<iframe width="560" height="315" src="https://www.youtube.com/embed/IMySm5q617o?rel=0&amp;showinfo=0&amp;start=393&amp" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

* In newer version you can also use the new ```CSWSequenceFromInputArray()``` in the minute **11:20**.
{: .notice--info}