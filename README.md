# Requirements

Python 2.6+

# Installation

Put "hydna" somewhere on your path.

# Usage

## Pushing Behaviors

To push behaviors, navigate to the folder holding your `setup.be` file and
issue the following command:

    hydna push --api-key=<api key> --domain=<domain name>

## Restarting an instance

You can manually restart a runnint instance (disconnecting all clients and
resetting state in Behaviors) with:

    hydna restart --api-key=<api key> --domain=<domain name>

# Configuration

When you run `hydna`, the tool will look for a configuration file named
`.hydna.conf` in the current working directory. If such a file exists, it
will be read and the settings found will be used when issuing subcommands.

You can also specify a path to a config file to be read using the switch
`--config-file`.

## Format

Settings are made up from key-value-pairs separated by an equal sign (`=`).

## Available settings

`path` - Path to the directory containing your `setup.be`

`api_key` - Your API key. The presence of this setting allows you to issue
            commands without the need to specify a key using `--api-key`.

`domain_name` - Name of the domain on which you wish to perform actions.
                The presence of this setting allows you to issue
                commands without the need to specify a domain using 
                `--domain`.

## Example config

    path = "./behaviors/"
    api_key = "i'm a secret"
    domian_name = "public.hydna.net"

# TODO

- Implement cert verification
- Add rest of commands
- Comment :)
