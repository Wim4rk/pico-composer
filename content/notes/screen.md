---
Title: Screen
Description: Screen sessions in Linux terminal
Template: note
Date: 2021-06-26
---

# Screen

Ok, so you'd like to run a command or start a service that will be running for
a long time, but not have a terminal window open to monitor it. I do this when
I start certain servers on remote machines.

We'll use `screen`. Just enter it into your teminal and we should have a session
running. If not, make sure `screen` is installed. It's easy to install.

`sudo apt install screen`

When you have an open screen session you can enter screen commands using ctrl+a
first. For example ctrl+a folowed by ? will list the available commands.

## Name your sessions

It's smart to name your sessions. It helps when you run multiple sessions. Use
descriptive names.

`session -S session_name`

## Inside a session

A session opens a terminal prompt. You can do anything there that you would do
in a "normal" terminal session. The advantage is the option to detach from the
current session. `ctrl+a d` will put your screen session in the background and
give you the usual terminal prompt back. Everything inside your screen session
keeps on running.

## Reattach to screen

`screen -r` will resume your screen session. If you have several sessions
running you'll need to append the session ID after the -r switch. `screen -r
session_name`

## List sessions

Pretty obvious: `screen -ls`.

##

Screen takes its config parameters from /etc/screenrc and ~/.screenrc (if
present). Modify it to your prefences.
