---
type: docs
title: "rad run CLI reference"
linkTitle: "rad run"
slug: rad_run
url: /reference/cli/rad_run/
description: "Details on the rad run Radius CLI command"
---
## rad run

Run an application

### Synopsis

Run an application specified by a Bicep or ARM template
	
The run command compiles a Bicep or ARM template and runs it in your default environment (unless otherwise specified). It also automatically port-forwards container ports and streams container logs to a user's terminal.
		
The run command accepts the same parameters as the 'rad deploy' command. See the 'rad deploy' help for more information.
	

```
rad run [file] [flags]
```

### Examples

```

# Run app.bicep
rad run app.bicep

# Run in a specific environment
rad run app.bicep --environment prod

# Run app.bicep and specify a string parameter
rad run app.bicep --parameters version=latest

# Run app.bicep and specify parameters from multiple sources
rad run app.bicep --parameters @myfile.json --parameters version=latest

```

### Options

```
  -a, --application string       The application name
  -e, --environment string       The environment name
  -g, --group string             The resource group name
  -h, --help                     help for run
  -p, --parameters stringArray   Specify parameters for the deployment
  -w, --workspace string         The workspace name
```

### Options inherited from parent commands

```
      --config string   config file (default "$HOME/.rad/config.yaml")
  -o, --output string   output format (supported formats are json, table) (default "table")
```

### SEE ALSO

* [rad]({{< ref rad.md >}})	 - Radius CLI

