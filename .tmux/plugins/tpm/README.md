# Tmux Plugin Manager

[![Build Status](https://travis-ci.org/tmux-plugins/tpm.png?branch=master)](https://travis-ci.org/tmux-plugins/tpm)

Installs and loads TMUX plugins.

### Installation

Requirements: `tmux` version 1.9 (or higher), `git`, `bash`.

Clone TPM:

    $ git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm

Put this at the bottom of `.tmux.conf`:

    # List of plugins
    set -g @plugin 'tmux-plugins/tpm'
    set -g @plugin 'tmux-plugins/tmux-sensible'

    # Other examples:
    # set -g @plugin 'github_username/plugin_name'
    # set -g @plugin 'git@github.com/user/plugin'
    # set -g @plugin 'git@bitbucket.com/user/plugin'

    # Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
    run '~/.tmux/plugins/tpm/tpm'

Reload TMUX environment so TPM is sourced:

    # type this in terminal
    $ tmux source ~/.tmux.conf

That's it!

(**Note:** using `set -g @tpm_plugins` is deprecated, but still works alongside
new syntax)

### Installing plugins

1. add new plugin to `.tmux.conf` with `set -g @plugin '...'`
2. hit `prefix + I` (I as in **I**nstall) to fetch the plugin

You're good to go! The plugin was cloned to `~/.tmux/plugins/` dir and sourced.

### Uninstalling plugins

1. remove (or comment out) plugin from the list
2. hit `prefix + alt + u` (u as in **u**ninstall) to remove the plugin

All the plugins are installed to `~/.tmux/plugins/` so alternatively you can
find plugin directory there and remove it.

### Key bindings

`prefix + I`
- installs new plugins from github or any other git repo
- refreshes TMUX environment

`prefix + U`
- updates plugin(s)

`prefix + alt + u`
- remove/uninstall plugins not on the plugin list

### More plugins

For more plugins, check [here](https://github.com/tmux-plugins).

### Docs

- [Help, tpm not working](docs/tpm_not_working.md) - problem solutions

More advanced features and instructions, regular users probably do not need
this:

- [How to create a plugin](docs/how_to_create_plugin.md). It's easy.
- [Managing plugins via the command line](docs/managing_plugins_via_cmd_line.md)
- [Changing plugins install dir](docs/changing_plugins_install_dir.md)
- [Automatic TPM installation on a new machine](docs/automatic_tpm_installation.md)

### Tests

Tests for this project run on [travis](https://travis-ci.org/tmux-plugins/tpm).

When run locally, [vagrant](https://www.vagrantup.com/) is required.
Run tests with:

    # within project directory
    $ ./run_tests

### Other goodies

- [tmux-copycat](https://github.com/tmux-plugins/tmux-copycat) - a plugin for
  regex searches in tmux and fast match selection
- [tmux-yank](https://github.com/tmux-plugins/tmux-yank) - enables copying
  highlighted text to system clipboard
- [tmux-open](https://github.com/tmux-plugins/tmux-open) - a plugin for quickly
  opening highlighted file or a url
- [tmux-continuum](https://github.com/tmux-plugins/tmux-continuum) - automatic
  restoring and continuous saving of tmux env

You might want to follow [@brunosutic](https://twitter.com/brunosutic) on
twitter if you want to hear about new tmux plugins or feature updates.

### License

[MIT](LICENSE.md)
