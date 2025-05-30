# velocilogic

A new CLI generated with oclif

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/velocilogic.svg)](https://npmjs.org/package/velocilogic)
[![Downloads/week](https://img.shields.io/npm/dw/velocilogic.svg)](https://npmjs.org/package/velocilogic)

<!-- toc -->
* [velocilogic](#velocilogic)
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->

# Usage

<!-- usage -->
```sh-session
$ npm install -g velocilogic
$ velocilogic COMMAND
running command...
$ velocilogic (--version)
velocilogic/0.1.0 linux-x64 node-v20.19.1
$ velocilogic --help [COMMAND]
USAGE
  $ velocilogic COMMAND
...
```
<!-- usagestop -->

# Commands

<!-- commands -->
* [`velocilogic help [COMMAND]`](#velocilogic-help-command)
* [`velocilogic plugins`](#velocilogic-plugins)
* [`velocilogic plugins add PLUGIN`](#velocilogic-plugins-add-plugin)
* [`velocilogic plugins:inspect PLUGIN...`](#velocilogic-pluginsinspect-plugin)
* [`velocilogic plugins install PLUGIN`](#velocilogic-plugins-install-plugin)
* [`velocilogic plugins link PATH`](#velocilogic-plugins-link-path)
* [`velocilogic plugins remove [PLUGIN]`](#velocilogic-plugins-remove-plugin)
* [`velocilogic plugins reset`](#velocilogic-plugins-reset)
* [`velocilogic plugins uninstall [PLUGIN]`](#velocilogic-plugins-uninstall-plugin)
* [`velocilogic plugins unlink [PLUGIN]`](#velocilogic-plugins-unlink-plugin)
* [`velocilogic plugins update`](#velocilogic-plugins-update)

## `velocilogic help [COMMAND]`

Display help for velocilogic.

```
USAGE
  $ velocilogic help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for velocilogic.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.2.28/src/commands/help.ts)_

## `velocilogic plugins`

List installed plugins.

```
USAGE
  $ velocilogic plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ velocilogic plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.38/src/commands/plugins/index.ts)_

## `velocilogic plugins add PLUGIN`

Installs a plugin into velocilogic.

```
USAGE
  $ velocilogic plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into velocilogic.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the VELOCILOGIC_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the VELOCILOGIC_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ velocilogic plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ velocilogic plugins add myplugin

  Install a plugin from a github url.

    $ velocilogic plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ velocilogic plugins add someuser/someplugin
```

## `velocilogic plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ velocilogic plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN...  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ velocilogic plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.38/src/commands/plugins/inspect.ts)_

## `velocilogic plugins install PLUGIN`

Installs a plugin into velocilogic.

```
USAGE
  $ velocilogic plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into velocilogic.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the VELOCILOGIC_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the VELOCILOGIC_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ velocilogic plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ velocilogic plugins install myplugin

  Install a plugin from a github url.

    $ velocilogic plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ velocilogic plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.38/src/commands/plugins/install.ts)_

## `velocilogic plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ velocilogic plugins link PATH [-h] [--install] [-v]

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ velocilogic plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.38/src/commands/plugins/link.ts)_

## `velocilogic plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ velocilogic plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ velocilogic plugins unlink
  $ velocilogic plugins remove

EXAMPLES
  $ velocilogic plugins remove myplugin
```

## `velocilogic plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ velocilogic plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.38/src/commands/plugins/reset.ts)_

## `velocilogic plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ velocilogic plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ velocilogic plugins unlink
  $ velocilogic plugins remove

EXAMPLES
  $ velocilogic plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.38/src/commands/plugins/uninstall.ts)_

## `velocilogic plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ velocilogic plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ velocilogic plugins unlink
  $ velocilogic plugins remove

EXAMPLES
  $ velocilogic plugins unlink myplugin
```

## `velocilogic plugins update`

Update installed plugins.

```
USAGE
  $ velocilogic plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.38/src/commands/plugins/update.ts)_
<!-- commandsstop -->
