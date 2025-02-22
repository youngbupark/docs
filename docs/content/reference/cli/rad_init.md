---
type: docs
title: "rad init CLI reference"
linkTitle: "rad init"
slug: rad_init
url: /reference/cli/rad_init/
description: "Details on the rad init Radius CLI command"
---
## rad init

Initialize Radius

### Synopsis


Interactively install the Radius control-plane and setup an environment.

If an environment already exists, 'rad init' will prompt the user to use the existing environment or create a new one.

By default, 'rad init' will optimize for a developer-focused environment with an environment named "default" and Recipes that support prototyping, development and testing using lightweight containers. These environments are great for building and testing your application.

Specifying the '--full' flag will cause 'rad init' to prompt the user for all available configuration options such as Kubernetes context, environment name, and cloud providers. This is useful for fully customizing your environment.


```
rad init [flags]
```

### Examples

```

## Create a new development environment named "default"
rad init

## Prompt the user for all available options to create a new environment
rad init --full

```

### Options

```
      --full            Prompt user for all available configuration options
  -h, --help            help for init
  -o, --output string   output format (supported formats are json, table) (default "table")
```

### Options inherited from parent commands

```
      --config string   config file (default "$HOME/.rad/config.yaml")
```

### SEE ALSO

* [rad]({{< ref rad.md >}})	 - Radius CLI

