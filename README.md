## Synposis

This package provides simple CLI functionality for use in Quali CloudShell field solutions.
For a more comprehensive package, check out the [cloudshell-cli](https://github.com/QualiSystems/cloudshell-cli) package.

## Installation

The best way is to just add this package to your python environment/driver.
So either:
`pip install qualilab_cli`
or add this package to the requirements.txt file of your driver.

## Code Example

```python
from QualiLab_CLI.Cli_Lib import Cli

session = Cli('localhost', 22, 'Telnet', 'USERNAME', 'PASSWORD', prompt_list=['.*>', '.*]', '.* ENTER'])

session.login()

result = session.send_and_receive('cli command')

print result
```

## Motivation

Making CLI connections, sending commands, matching patterns, receiving output is the most commone operation
for Quali CloudShell shells.  This package simplifies this, and provides a unified interface for using either
Telnet or SSH
