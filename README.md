# Requirements

Python 2.6+

(the tool will work with versions prior to 2.6 (tested with 2.5.2) if
simplejson is installed)

# Installation

There are a few different ways to install the tool. Please note that your
$PATH must include the path to the directory into which Python executables
are installed.

## Option 1 - easy_install

    sudo easy_install hydna-cli

## Option 2 - pip

    pip install hydna-cli

## Option 3 - Manual install

You can also manually put the tool in a directory on your path by
downloading the script from:

    https://raw.github.com/hydna/hydna-cli/master/hydna

# Usage

## Pushing Behaviors

To push behaviors, navigate to the folder holding your `setup.be` file and
issue the following command:

    hydna push --api-key=<api key> --domain-name=<domain name>

## Restarting an instance

You can manually restart a runnint instance (disconnecting all clients and
resetting state in Behaviors) with:

    hydna restart --api-key=<api key> --domain-name=<domain name>

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
                `--domain-name`.

## Example config

    path = "./behaviors/"
    api_key = "i'm a secret"
    domian_name = "public.hydna.net"

# TODO

- Consistent - and more helpful - output from commands
- Implement cert verification
- Add rest of commands
- Add docstrings and comments
- Attempt to locate config file in parent(s) a la git?
