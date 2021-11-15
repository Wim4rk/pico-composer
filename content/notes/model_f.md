---
Title: Using an IBM Model F
Description: Adventure in protocols and keymaps
Date: 2021-06-25
Template: note
---

# Flashing a Soarer's converter in linux

Wanted to make the definitive guide. Please let me know what I've missed. Found a lot of guides on how to do it on Windows. Well, this is almost the same
thing, only we need to address the things that aren't. Linux don't deal with .bat-files for starter, so we need to write bash commands.

So, we've got this cool, cool keyboard we'd like to actually use. We need to make it talk to our computer, and we'd like to mitigate one
or two drawbacks of the board itself. This keyboard doesn't have a lot of keys to begin with.

Soarer's converter is easy to use, but it has a few drawbacks. I'll tell you about that at the end of the article.

## Setup

In this case I'm using a Linux terminal (Debian style). My keyboard is an IBM model F/XT. I use a commersial Soarer's converter.

Got error message:
`error while loading shared libraries: libstdc++.so.6: cannot open shared object file: No such file or directory`

Both mean that you're on a 64-bit system. You need to install 32-bit versions.

Tried downloading a few different variants for this, but the one command that worked was ` sudo apt-get install lib32stdc++6`

Also `error while loading shared libraries: libusb-0.1.so.4: cannot open shared object file: No such file or directory`

And `sudo apt-get install libusb-0.1-4:i386`. You might need to enable foreign architecture: `sudo dpkg --add-architecture i386`, check if it's there first: `sudo dpkg --print-foreign-architecture`. I've tested this on Ubuntu and Debian.

This is where I started wondering if it's really worth it? I just decided no.

Could then make scb-file with ` sudo ./scas empty.sc empty.scb`

To finally move the file onto the converter:

## Building

### Tools

Make sure the tools are executable:

```
$ sudo chmod +x scas scboot scdis scinfo scrd scwr
```

Soarer's converter assembler `scas`.  Takes two arguments; file to be buildt and the new file name. File ending should be `.scb`. Will kindly show (rather useless) errors.

`$ sudo ./scas remap.sc new_file.scb`

But what if: `sudo: kunde inte köra ./scas: Filen eller katalogen finns inte`? Debian isn't as friendly as Ubuntu. I needed to do the update above. libusb och lib32stdc.

Creates a file we're to write to the converter.

## Flashing

Soarer's converter writer `scwr`

`$ sudo ./scwr new_file.scb`

Probably no trouble. File's been checked.


## The IBM Model F-XT

This is a ver ynice board in deed, but it has a few quirks. For starters, we are missing a few keys. The GUI (off course), an Alt Gr if you need one. And there is no navcluster.

The navcluster on the num-pad doesn't really do what you'd think it does. If you'd like to mark a few characters and press alt + left (the number 4 key), you get a four in stead of a marked character to the left. A way around this is to remap the num_lock to select a second layer

`Example`

And then to remap the numpad with actual navcluster keys.

`Example`

On the second layer we reset the numpad.

`Example`

## Key spamming

Probably due to wrong voltage. In my case it was ground. I've opened the board a couple of times, and obviously on the last attempt I hadn`t managed to attach the ground properly. It's supposed to go between the top- and bottom case, and you need to screw it down pretty thoroughly.

# HID-listener

Just download file, place in folder and from terminal `sudo chmod 755 hid_listen` and `sudo ./hid_listen`. If you seem to have a problem with 32-bit, you need to build software from source. Good luck!

# Drawbacks

So, there are a few things we need to talk about.

I would like a single key to do two different things when I click it, and when i hold it. That's impossible using Soarer's converter.

I can't output a certain character, in stead I need to make a key combo; e.g. { would be alt gr + 7.

I would like a key to output a combo. That takes writing a macro. If I'd like one key in a certain leyer to output a special character I'd have to create a macro, pressing mods, klicking key, releasing mods. It's a hassle. But you only need to do it once, I suppose.

(example be inserted here)
