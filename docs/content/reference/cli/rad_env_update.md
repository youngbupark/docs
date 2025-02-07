---
type: docs
title: "rad env update CLI reference"
linkTitle: "rad env update"
slug: rad_env_update
url: /reference/cli/rad_env_update/
description: "Details on the rad env update Radius CLI command"
---
## rad env update

Update environment configuration

### Synopsis

Update environment configuration
	
This command updates the configuration of an environment for properties that are able to be changed.
		
Properties that can be updated include:
- providers (Azure, AWS)
		  
All other properties require the environment to be deleted and recreated.


```
rad env update [environment] [flags]
```

### Examples

```

## Add Azure cloud provider for deploying Azure resources
rad env update myenv --azure-subscription-id **** --azure-resource-group myrg

## Add AWS cloud provider for deploying AWS resources
rad env update myenv --aws-region us-west-2 --aws-account-id *****

## Remove Azure cloud provider
rad env update myenv --clear-azure

## Remove AWS cloud provider
rad env update myenv --clear-aws

```

### Options

```
      --aws-account-id string          The account ID where AWS resources will be deployed
      --aws-region string              The region where AWS resources will be deployed
      --azure-resource-group string    The resource group where Azure resources will be deployed
      --azure-subscription-id string   The subscription ID where Azure resources will be deployed
      --clear-aws                      Specify if aws provider needs to be cleared on env
      --clear-azure                    Specify if azure provider needs to be cleared on env
  -e, --environment string             The environment name
  -g, --group string                   The resource group name
  -h, --help                           help for update
  -o, --output string                  output format (supported formats are json, table) (default "table")
  -w, --workspace string               The workspace name
```

### Options inherited from parent commands

```
      --config string   config file (default "$HOME/.rad/config.yaml")
```

### SEE ALSO

* [rad env]({{< ref rad_env.md >}})	 - Manage Radius Environments

