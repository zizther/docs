# 1. Install Craft CMS

We’ll start by installing Craft CMS directly on your computer in a local _development environment_.

Craft is a web application that needs to run on web server, and a local development environment provides that web server’s software on your personal workstation. This way, we can work with Craft freely and privately without the need to set up a hosting account. ([We’ll get to that later](../deploy/README.md).)

You’re going to need three things to get up and running, and we’ll take a look at each one in detail:

1. The console utility that’s built into your operating system.
2. A web server that meets [Craft’s minimum requirements](https://docs.craftcms.com/v3/requirements.html).
3. A code editor.

## Get to know your console

Every operating system comes with a text-based command line interface (CLI) for inputting commands. This provides a powerful way of doing lots of things beyond whatever the graphical user interface facilitates. 

::: tip
If you’ve time traveled from the past, your operating system may *only* have a command line interface. Our GUIs are going to blow your mind.
:::

We’ll be installing Craft with an application called [Composer](https://getcomposer.org/) that’s only available from the console—but don’t worry, it’s worth it!

### Find your OS console

TODO: add default icons and terminal screenshots from each OS

- On MacOS, the default console is Terminal.app.
- On Windows, the default console is called Command Prompt.
- On Ubuntu Linux, the default console is called Terminal.

### Run a command

Once you’ve launched your console, you’ll be greeted by an empty prompt. Later on we’ll refer to “running” commands that’ll look like this:

```bash
echo "hello world"
```

In this example, you would copy+paste or type `echo "hello world"` exactly as you see it above, then hit <kbd>return</kbd> or <kbd>enter</kbd> to execute the command. The result, or output, will be printed and you’ll be returned to the empty prompt—that’s all the `echo` command does!

Here’s what you'd see after running that command:

```bash
echo "hello world"
hello world
```

You can learn more about working with your console in MacOS, Windows, or Linux. If you were able to open your console and run the “hello world” command, you’re ready to continue!

## Choose a code editor

The files Craft installs on your computer are all stored in plain text. 

There are a few benefits to plain text files, one being they’re extremely portable: you don’t need any special software to open and edit them, so anyone working with your site’s code could use whatever application they’d prefer. We’ll start editing a few of these files to configure our site, and others later to customize what it looks like.

While you could get away with using TextEdit.app, Notepad, or Text Editor, it’s a good idea to first choose a code editor because it’ll make things easier later on. Code editors...

- make it easy to work with multiple files
- add color coding and helpful tools depending on the file type you’re working with
- handle invisible characters like spaces and returns carefully, which can cause annoying problems across operating systems

An excellent and popular code editor is [Visual Studio Code](https://code.visualstudio.com/), which is available for free on MacOS, Windows, and Linux.

More advanced PHP developers tend to use [PhpStorm](https://www.jetbrains.com/phpstorm/), which is a more complex and specialized commercial Integrated Development Environment (IDE) specifically geared toward PHP development.

There are plenty of other options you’re free to use, just know that the rest of our steps and screenshots in this tutorial will assume you’re using VS Code.

## Set up a development environment

The word “environment” here refers to the software that’s needed to work with Craft CMS, which is detailed in [Craft’s minimum requirements](https://docs.craftcms.com/v3/requirements.html). 

Like your workstation, a web server can run different operating systems and applications. Web servers, however, are commonly configured with specific combinations of software for the types of applications they’re meant to run. These combinations are referred to as “stacks”. (You’ve probably heard of a “full stack developer”, which means someone has experience with each of the software components in a particular stack.)

Craft can run on a number of different stacks, but the main ingredients are...

- **PHP**: the programming language in which Craft is written.
- **A database**: the place where content and most information is stored, sort of like a collection of Excel files that are used by code and able to store and retrieve lots of data quickly. Commonly MySQL or PostgreSQL.
- **A web server**: the software that listens for requests made by your web browser, hands them off to a web application, and returns the application’s response back to the browser. Commonly Apache or nginx.

The best way to get working quickly is to use a pre-packaged web server that runs on your operating system. The good news is that you’ve got plenty of options no matter your OS. The bad news is that the _best_ option depends on what OS you’re using and whatever software you’ve already installed.

Choose one of the following guides to set up a development environment on your OS.

TODO: write environment setup guides for each (must include creating a database + what settings Craft needs + how to run console commands)

### MacOS, Windows, and Linux

- [Laravel Homestead](#)
- [Vagrant](#)
- [DDEV](#)
- [Lando](#)

### MacOS

- [MAMP](#)
- [Laravel Valet](#)

### Windows

- [AMPPS](#)
- [XAMPP](#)

::: tip
If you’re not sure where to start, MAMP and XAMPP are easiest options to start with on MacOS and Windows. Laravel Homestead and Laravel Valet are worth the extra time commitment if you’ll be working a lot more with PHP.
:::

## Install Craft CMS with Composer

At this point you should have a local development environment running with a database and know how to use console commands. Now we’ll make sure Composer is installed.

### What's Composer?

Composer is a command line application with one important job: it makes sure our website has all the PHP code it needs to run.

This code is split up into numerous _packages_ written by different authors. Our website depends on these packages—also referred to as _dependencies_—and each one provides a specific set of functionality. Composer makes sure every PHP package (including Craft CMS!) is installed, has the dependencies it needs to do its job, and that all these packages can work together without major conflicts.

Composer handles the complexity of combining these packages so we can use the best software available for each individual job the website needs to accomplish.

### Check your Composer version

Try running the following console command:

```bash
composer --version
```

This will print your current Composer version if it’s installed, or `command not found` if Composer is not installed.

If you’re using Composer 1.3.0 or higher, you’re ready to [Install Craft CMS via Composer](#install-craft-cms-via-composer). If you’re running a lower version or haven’t installed Composer, see [Composer’s install guide](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-macos).

::: tip
You may be able update your Composer version by runing `composer self-update`. If that doesn’t work, follow the installation instructions to install a newer version.
:::

### Install Craft CMS via Composer

Choose a new path on your computer where you’d like to install Craft CMS. You’ll need to either provide a full path (like `/Users/lucille/projets/craft`) or navigate to an existing folder using the `cd` terminal command and providing the name of a new relative folder to be created from there.

Either way, subsitute your desired path for `<Path>` in this command:

```bash
composer create-project craftcms/craft <Path>
```

Composer will take a few minutes to download Craft CMS and all its dependencies, set up your project folders, and a security key:

TODO: add animation of install process

### Tour the site’s folder structure

TODO: tour file structure

### Finish setup

TODO: confirm web server points to `web/` and DB settings are set per environment setup guide

#### From the terminal

TODO: write this

#### From a web browser

TODO: write this
