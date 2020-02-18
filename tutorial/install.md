# 1. Install Craft CMS

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
