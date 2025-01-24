---
title: "About dbt invocation command"
sidebar_label: "invocation"
id: invocation
---

The `dbt invocation` command enables you to view active invocations when sessions are taking too long to execute or when you get a `Session occupied` error in the dbt Cloud CLI. This command is useful for debugging long-running or 'hanging' sessions. This command isn't needed for completed sessions (sessions that have completed running).

This page lists the command and flag you can use with `dbt invocation` in the [dbt Cloud CLI](/docs/cloud/cloud-cli-installation). To use them, add a command or option like this: `dbt invocation [flag]`.

Available flags in the command line interface (CLI) are [`help`](#dbt-invocation-help) and [`list`](#dbt-invocation-list).

## Usage

The following examples show how to use the `dbt invocation` command in the dbt Cloud CLI using the `help` and `list` flags.

### dbt invocation help

The `help` command provides you with the help output for the `invocation` command in the CLI, including the available flags.

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

### dbt invocation list

The `list` command provides you with a list of active invocations in your dbt Cloud CLI. When a long-running session is active, you can use this command in a separate terminal window to view the active session and its status.

```shell
dbt invocation list
```

The command returns the following information, including the `ID`, `status`, `type`, `arguments`, and `started at` time of the active session:

```bash
dbt invocation list

Active Invocations:
  ID                             6dcf4723-e057-48b5-946f-a4d87e1d117a
  Status                         running
  Type                           cli
  Args                           [run --select test.sql]
  Started At                     2025-01-24 11:03:19

➜  jaffle-shop git:(test-cli) ✗ 
```
