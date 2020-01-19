---
title: Copy and Pasting on the new Windows Terminal
date: "2020-01-18T23:46:37.121Z"
template: "post"
draft: false
slug: "copy-and-pasting-on-the-new-windows-terminal"
category: "HOW-TOS"
tags:
  - "Windows"
  - "The More You Know"
description: "How to make CTRL-C and CTRL-V work on the new Windows Terminal."
socialImage: "/media/new-win-terminal.png"
---

In May of 2019, Microsoft announced a new terminal for Windows.  Twelve seconds into the [video preview](https://www.youtube.com/watch?v=8gw0rXPMMPE) and I was completely sold.  Fast forward to today, I finally got a chance to try the preview release.  Having used iTerm on macOS for years my fingers kept wanting to use the OS default key bindings as opposed to `CTRL+Shift+C` and `CTRL+Shift+V`.  Muscle memory is a powerful thing indeed. Anyways, here's what I did to address this problem.

1. Press `CTRL+,` to open `profiles.json`. 
2. Add the following entries to the `keybindings` array:
  ```json
  {
  	"command": "copy",
  	"keys": ["ctrl+c"]
  },
  {
  	"command": "paste",
  	"keys": ["ctrl+v"]
  }
  ```

And there you have it. 

In case you are wondering, when nothing is highlighted `CTRL+C` will continue to work as an interrupt signal to any running task. The terminal app is smart enough to differentiate between the two scenarios. 



