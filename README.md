# Overview

The default plugin repository for [Naomi](https://github.com/naomiproject/naomi).

The `plugins.csv` file in this repo is effectively the list of all plugins that Naomi can see.

When Naomi boots up, it attempts to enable all the plugins specified in it's configuration file.
If a plugin is not found locally, Naomi will fetch the plugin based on it's entry in the `plugins.csv` file (if found).

The database `plugins.cvs` file is broken down into five different columns. Plugin profile.yml Name, Plugin Display Name, Category, Plugin Description, Plugin Repo Link.

Categories available:

* Audioengine
* Speechhandler
* STT (speech to text)
* STT_Trainer
* TTI (text to intent)
* TTS (text to speech)
* VAD
* Visualizations

The file is also parsed by [Naomi UI Plugins](https://github.com/naomiproject/)
and list the available plugins for the user to download through the Naomi
client.

If you wish to add your plugin to the default plugin repository, create a
[pull request](https://github.com/naomiproject/naomi-plugins/compare) with your
addition in the plugins.csv file.

Please keep the file in alphabetical order.

## Plugin Developers

By default, Naomi will clone new plugins in the following directory: `~/.config/naomi/plugins`

This can be configured in `profile.yml`:

    # The local directory holding all existing (and downloaded) plugins.
    plugin_directory = '~/.config/naomi/plugins'

Developers can go directly into that directory to create new plugins, code, and make changes to existing plugins.

See the [plugin development guide](https://projectnaomi.com/dev/docs/developer/plugins)
for more information on creating your own Naomi plugins.

## Private Plugins

You can easily search for and download plugins using the [Naomi Plugin Exchange](https://projectnaomi.com/dev/docs/plugins/).

You can also activate custom plugins by simply dropping them in the configured
`plugin_directory`.

We always appreciate contributions and new plugin submissions. If you made
Naomi better through a private plugin, consider sharing the code.

We understand that it's more difficult to make a plugin for the public
than it is to make it for oneself. If you feel intimidated sharing your code,
don't know how to go about it, or think your plugin is too specialized, let us
know. There's a good chance we can help make your plugin (even more) awesome.
We'd love to help you contribute and grow Naomi's list of plugins.
