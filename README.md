oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g legalcast
$ legalcast COMMAND
running command...
$ legalcast (--version)
legalcast/0.0.0 darwin-arm64 node-v18.12.1
$ legalcast --help [COMMAND]
USAGE
  $ legalcast COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`legalcast hello PERSON`](#legalcast-hello-person)
* [`legalcast hello world`](#legalcast-hello-world)
* [`legalcast help [COMMANDS]`](#legalcast-help-commands)
* [`legalcast plugins`](#legalcast-plugins)
* [`legalcast plugins:install PLUGIN...`](#legalcast-pluginsinstall-plugin)
* [`legalcast plugins:inspect PLUGIN...`](#legalcast-pluginsinspect-plugin)
* [`legalcast plugins:install PLUGIN...`](#legalcast-pluginsinstall-plugin-1)
* [`legalcast plugins:link PLUGIN`](#legalcast-pluginslink-plugin)
* [`legalcast plugins:uninstall PLUGIN...`](#legalcast-pluginsuninstall-plugin)
* [`legalcast plugins:uninstall PLUGIN...`](#legalcast-pluginsuninstall-plugin-1)
* [`legalcast plugins:uninstall PLUGIN...`](#legalcast-pluginsuninstall-plugin-2)
* [`legalcast plugins update`](#legalcast-plugins-update)

## `legalcast hello PERSON`

Say hello

```
USAGE
  $ legalcast hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/legalmentedev/legalcast-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `legalcast hello world`

Say hello world

```
USAGE
  $ legalcast hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ legalcast hello world
  hello world! (./src/commands/hello/world.ts)
```

## `legalcast help [COMMANDS]`

Display help for legalcast.

```
USAGE
  $ legalcast help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for legalcast.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.9/src/commands/help.ts)_

## `legalcast plugins`

List installed plugins.

```
USAGE
  $ legalcast plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ legalcast plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.4.4/src/commands/plugins/index.ts)_

## `legalcast plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ legalcast plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ legalcast plugins add

EXAMPLES
  $ legalcast plugins:install myplugin 

  $ legalcast plugins:install https://github.com/someuser/someplugin

  $ legalcast plugins:install someuser/someplugin
```

## `legalcast plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ legalcast plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ legalcast plugins:inspect myplugin
```

## `legalcast plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ legalcast plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ legalcast plugins add

EXAMPLES
  $ legalcast plugins:install myplugin 

  $ legalcast plugins:install https://github.com/someuser/someplugin

  $ legalcast plugins:install someuser/someplugin
```

## `legalcast plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ legalcast plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ legalcast plugins:link myplugin
```

## `legalcast plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ legalcast plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ legalcast plugins unlink
  $ legalcast plugins remove
```

## `legalcast plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ legalcast plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ legalcast plugins unlink
  $ legalcast plugins remove
```

## `legalcast plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ legalcast plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ legalcast plugins unlink
  $ legalcast plugins remove
```

## `legalcast plugins update`

Update installed plugins.

```
USAGE
  $ legalcast plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
