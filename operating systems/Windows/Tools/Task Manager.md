---
tags:
  - os
  - windows
  - utility
---
# Task Manager

The thing you know and love. However, you probably only use this to kill applications or monitor the usage of your CPU, GPU or internet connection.

## Features

These are various tools built into Task Manager to view processes and control them.

### Processes

These are all the running processes on your machine, whether they are applications (the Apps header), background processes (the Background processes header (yes, it's not capital case)) or Windows processes (the Windows processes header).

You can add or remove columns/metrics to view more about the processes and what resources they are consuming. Columns include:

- CPU usage
- GPU usage
- PID
- disk usage
- network usage
- power usage

Finally, you can kill a task with the `End Task` button on the bottom right.

### Performance

These are graphs to show the usage of your CPU, memory, disk, internet connection, etc. in real time.

### Startup

These are all the processes that start when you log into an account things like:

- discord
- one drive
- cortana
- drivers

No way to search the startup processes for keywords or strings however.

### Users

This is a way to see all the processes used by each user and the resources they are consuming. From this tab, you can disconnect a user from the system or manager the user's settings.

### Services

These are background processes like daemons on Linux, you can start, stop, restart and inspect these services to figure out what they can do.

>Imagine a GUI for `systemctl` on Linux, or whatever init system you use.
