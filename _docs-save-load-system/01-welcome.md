---
title: "Welcome"
permalink: /docs-save-load-system/welcome/
excerpt: "How to quickly install and setup Minimal Mistakes for use with GitHub Pages."
last_modified_at: 2017-11-15T09:49:52-05:00
redirect_from:
  - /theme-setup/
toc: true
---

Hi!, welcome to the documentation of the "CSW Autosave and Load System w/compression" plugin for Unreal Engine 4. If you want to purchase the plugin, watch the description page or download the project example, please refer to: https://www.unrealengine.com/marketplace/csw-autosave-and-load-system-w-compression

## About the plugin

This product is a C++ plugin for Unreal Engine 4. But although the plugin is written in C++ all the functionality can be used in Blueprints very easily. This plugin is mainly aimed to indie solo or team developers but it can be easily escalated to bigger projects, specially considering that the source code is accessible and well commented.

The plugin is developed with a "generic-programming pattern" in mind, in a way that it can be used in all kind of project. It's so flexible in fact, that it can even used for features for which wasn't even designed; such as an undo/redo system, cloud saving system (the compression feature plays a big role in this one), etc.

Of course, the main goal of the plugin is to simplify the implementation of a Save and Load system in your game. To achieve that, the plug-in is very straight forward in the way it works and it's easy to understand. In fact, if you already have implemented a save and load system using the built-in features from Unreal Engine before, you'll see that this plugin is not very different. Actually, this plugin extends from the Unreal Engine features so you can still use the logic you've implemented (SaveGameToSlot(), LoadGameFromSlot(), change the parent of your Save Game Object, etc.).

If you haven't yet implemented a Save and Load system in your game, fear not! This documentation is aimed for beginners and advanced users (for advanced users, mainly the customization part). If you have problems following the documentation, i have also created some nice video tutorials: https://www.youtube.com/watch?v=IMySm5q617o&index=2&list=PL7Se41ZzAKZmPVJGCaFxv1bPMXqPgEOQa which i hope you'll enjoy.

### Why buy this plugin?

I know, if you're here then you probably already bought the plugin. But one can never know. If you're wondering why would you buy this plugin in the first place then i have a very nice list or reasons right here:

* Much of the save and load work is done behind the scenes. You don't have to worry about the complexity of a save system but only about how you want to implement the system in your game. Not all the games use the same save and load system but this plugin is designed in a way that can be adapted to pretty much any game!
* Very easy to use. You add a component to the Actors you want to save, call the saving functions when you want, call the load functions when you want and that's it! At least the basic functionality. The plugin even auto handle for you the Transforms and the Physics simulation states of your Actors (position, rotation and velocity) so you don't have to worry about that. Of course, you can disable this auto-functionality any time for any Actor and even in runtime.
* Customizable component. If you attach my component to an Actor, you'll be able to customize (even in runtime) the way this actor will be saved and loaded. By default you can save even the components and child Actor components from the Actor or you can set which components you want or you don't want to be saved.
* Save Variables in a breeze. Even for components. You only have to check a property for the variables you want to save, it's that easy.
* Customizable Global Save and Load functions. You can just use this: TODO ADD IMAGE for saving and loading your game which will be enough for many games. But if your game needs to be saved and loaded in a very specific way, then this plugin also exposes functions for how the global save and load functionality will work. It even supports level streaming!
	
	The global functions for saving and loading are static functions. This means that those functions can be called from anywhere (Actors, UIs, etc.). The functions can also be called as many times as you want (for saving specific data that will be excluded from the main data for example).
	{: .notice--info}
* Fast! The plugin is written in C++ so it's really fast.
* It has a compression feature. This will allow you to keep your save files very small in size. Why would you want that? For implementing a cloud save and load system of course! You can convert your save object into a compressd String and send it to a cloud provider, like this: TODO GAMESPARKS TUTORIAL. This plugin is so nice in fact, that can convert ANY object into a compressed string so you can actually send almost any UE4 data to the Internet (i.e Player Avatar's picture).

### GitHub Pages Compatible Methods

If you're hosting with GitHub Pages follow these steps instead.

**Note:** [jekyll-remote-theme](https://github.com/benbalter/jekyll-remote-theme) is currently in beta on GitHub Pages. In my tests it works as advertised, with the occasional failure due to missing `_includes` and `_layouts` --- your results may vary.
{: .notice--warning}

Replace `gem "jekyll"` with:

```
gem "github-pages", group: :jekyll_plugins
gem "jekyll-remote-theme"
```

Run `bundle update` and verify that all gems install properly.

Add `remote_theme: "mmistakes/minimal-mistakes"` to your `_config.yml` file.

Then add [`jekyll-remote-theme`](https://github.com/benbalter/jekyll-remote-theme) to the `plugins` (previously gems) array in your `_config.yml` file like so:

```
plugins:
  - jekyll-remote-theme
```

---

**Note:** Your Jekyll site should be viewable immediately at <http://USERNAME.github.io>. If it's not, you can force a rebuild by **Customizing Your Site** (see below for more details).
{: .notice--warning}

If you're hosting several Jekyll based sites under the same GitHub username you will have to use Project Pages instead of User Pages. Essentially you rename the repo to something other than **USERNAME.github.io** and create a `gh-pages` branch off of `master`. For more details on how to set things up check [GitHub's documentation](https://help.github.com/articles/user-organization-and-project-pages/).

<figure>
  <img src="{{ '/assets/images/mm-gh-pages.gif' | absolute_url }}" alt="creating a new branch on GitHub">
</figure>

You can also install the theme by copying all of the theme files[^structure] into your project.

To do so fork the [Minimal Mistakes theme](https://github.com/mmistakes/minimal-mistakes/fork), then rename the repo to **USERNAME.github.io** --- replacing **USERNAME** with your GitHub username.

<figure>
  <img src="{{ '/assets/images/mm-theme-fork-repo.png' | absolute_url }}" alt="fork Minimal Mistakes">
</figure>

**GitHub Pages Alternatives:** Looking to host your site for free and install/update the theme painlessly? [Netflify][netlify-jekyll], [GitLab Pages][gitlab-jekyll], and [Continuous Integration (CI) services][ci-jekyll] have you covered. In most cases all you need to do is connect your repository to them, create a simple configuration file, and install the theme following the [Ruby Gem Method](#ruby-gem-method) above.
{: .notice--info}

[netlify-jekyll]: https://www.netlify.com/blog/2015/10/28/a-step-by-step-guide-jekyll-3.0-on-netlify/
[gitlab-jekyll]: https://about.gitlab.com/2016/04/07/gitlab-pages-setup/
[ci-jekyll]: https://jekyllrb.com/docs/save-load-system/continuous-integration/

### Remove the Unnecessary

If you forked or downloaded the `minimal-mistakes-jekyll` repo you can safely remove the following folders and files:

- `.editorconfig`
- `.gitattributes`
- `.github`
- `/docs`
- `/test`
- `CHANGELOG.md`
- `minimal-mistakes-jekyll.gemspec`
- `README.md`
- `screenshot-layouts.png`
- `screenshot.png`

## Setup Your Site

Depending on the path you took installing Minimal Mistakes you'll setup things a little differently.

**ProTip:** The source code and content files for this site can be found in the [`/docs` folder](https://github.com/mmistakes/minimal-mistakes/tree/master/docs) if you want to copy or learn from them.
{: .notice--info}

### Starting Fresh

Starting with an empty folder and `Gemfile` you'll need to copy or re-create this [default `_config.yml`](https://github.com/mmistakes/minimal-mistakes/blob/master/_config.yml) file. For a full explanation of every setting be sure to read the [**Configuration**]({{ "/docs/save-load-system/configuration/" | absolute_url }}) section.

From `v4.5.0` onwards, Minimal Mistakes theme-gem comes bundled with the necessary data files and will automatically use them via the [`jekyll-data`](https://github.com/ashmaroli/jekyll-data) plugin. So you no longer need to maintain a copy of these data files at your project directory.

However like all other bundled files, you'll need to create and edit these data files to customize them.
The bundled data files are:

- [`_data/ui-text.yml`](https://github.com/mmistakes/minimal-mistakes/blob/master/_data/ui-text.yml) - UI text [documentation]({{ "/docs/save-load-system/ui-text/" | absolute_url }})
- [`_data/navigation.yml`](https://github.com/mmistakes/minimal-mistakes/blob/master/_data/navigation.yml) - navigation [documentation]({{ "/docs/save-load-system/navigation/" | absolute_url }})

### Starting from `jekyll new`

Scaffolding out a site with the `jekyll new` command requires you to modify a few files that it creates.

Edit `_config.yml`. Then:

- Replace `<site root>/index.md` with a modified [Minimal Mistakes `index.html`](https://github.com/mmistakes/minimal-mistakes/blob/master/index.html). Be sure to enable pagination if using the [`home` layout]({{ "/docs/save-load-system/layouts/#home-page" | absolute_url }}) by adding the necessary lines to **_config.yml**.
- Change `layout: post` in `_posts/0000-00-00-welcome-to-jekyll.markdown` to `layout: single`.
- Remove `about.md`, or at the very least change `layout: page` to `layout: single` and remove references to `icon-github.html` (or [copy to your `_includes`](https://github.com/jekyll/minima/tree/master/_includes) if using it).

### Migrating to Gem Version

If you're migrating a site already using Minimal Mistakes and haven't customized any of the theme files things upgrading will be easier for you.

Start by removing the following folders and any files within them: 

```terminal
├── _includes
├── _layouts
├── _sass
├── assets
|  ├── css
|  ├── fonts
|  └── js
```

You won't need these anymore as they're bundled with the theme gem --- unless you intend to [override them](http://jekyllrb.com/docs/save-load-system/themes/#overriding-theme-defaults).

**Note:** When clearing out the `assets` folder be sure to leave any files you've added and need. This includes images, CSS, or JavaScript that aren't already [bundled in the theme](https://github.com/mmistakes/minimal-mistakes/tree/master/assets). 
{: .notice--warning}

From `v4.5.0` onwards, you don't have to maintain a copy of the default data files viz. `_data/ui-text.yml` and `_data/navigation.yml` either.
The default files are read-in automatically via the [`jekyll-data`](https://github.com/ashmaroli/jekyll-data) plugin.

If you customized any of these files leave them alone, and only remove the untouched ones. If done correctly your modified versions should [override](http://jekyllrb.com/docs/save-load-system/themes/#overriding-theme-defaults) the versions bundled with the theme and be used by Jekyll instead.

#### Update Gemfile

Replace `gem "github-pages` or `gem "jekyll"` with `gem "jekyll", "~> 3.5"`. You'll need the latest version of Jekyll[^update-jekyll] for Minimal Mistakes to work and load all of the theme's assets properly, this line forces Bundler to do that.

[^update-jekyll]: You could also run `bundle update jekyll` to update Jekyll.

Add the Minimal Mistakes theme gem: 

```ruby
gem "minimal-mistakes-jekyll"
```

When finished your `Gemfile` should look something like this:

```ruby
source "https://rubygems.org"

gem "jekyll", "~> 3.5"
gem "minimal-mistakes-jekyll"
```

Then run `bundle update` and add `theme: minimal-mistakes-jekyll` to your `_config.yml`.

**v4 Breaking Change:** Paths for image headers, overlays, teasers, [galleries]({{ "/docs/save-load-system/helpers/#gallery" | absolute_url }}), and [feature rows]({{ "/docs/save-load-system/helpers/#feature-row" | absolute_url }}) have changed and now require a full path. Instead of just `image: filename.jpg` you'll need to use the full path eg: `image: /assets/images/filename.jpg`. The preferred location is now `/assets/images/` but can be placed elsewhere or externally hosted. This applies to image references in `_config.yml` and `author.yml` as well.
{: .notice--danger}

---

That's it! If all goes well running `bundle exec jekyll serve` should spin-up your site.
