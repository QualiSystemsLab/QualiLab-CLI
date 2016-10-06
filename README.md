## Synposis

This package provides CLI functionality for use in Quali CloudShell field solutions.

## Code Example

session = Cli('localhost', 22, 'Telnet', 'USERNAME', 'PASSWORD', prompt_list=['.*>', '.*]', '.* ENTER'])

session.login()

result = session.send_and_receive('cli command')

print result

## Motivation

Making CLI connections, sending commands, matching patterns, receiving output is the most commone operation
for Quali CloudShell shells.  This package simplifies this, and provides a unified interface for using either
Telnet or SSH
