---
title: "About dbt invocation command"
sidebar_label: "invocation"
id: invocation
---

The `dbt invocation` command enables you to view current active invocations. This is useful when you want to see the commands that have hanged or are taking too long.

- Viewing your local configuration details (account ID, active project ID, deployment environment, and more).
- Viewing your dbt Cloud configuration details (environment ID, environment name, connection type, and more).

This guide lists all the commands and options you can use with `dbt invocation` in the [dbt Cloud CLI](/docs/cloud/cloud-cli-installation). To use them, add a command or option like this: `dbt invocation [command]` or use the shorthand  `dbt inv [command]`.

### dbt invocation help

The `help` command allows you to view the help output for a specific command in your command line interface, including the available flags.

```shell
dbt invocation help
```

or 

```shell
dbt help invocation
```

The command returns the following information:

```bash
dbt invocation help
Manage invocations

Usage:
  dbt invocation [command]

Available Commands:
  list        List active invocations

Flags:
  -h, --help   help for invocation

Global Flags:
      --log-format LogFormat   The log format, either json or plain. (default plain)
      --log-level LogLevel     The log level, one of debug, info, warning, error or fatal. (default info)
      --no-color               Disables colorization of the output.
  -q, --quiet                  Suppress all non-error logging to stdout.

Use "dbt invocation [command] --help" for more information about a command.
```

