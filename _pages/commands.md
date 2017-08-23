---
layout: single
permalink: /commands.html
redirect_to:
  - http://docs.unrealcv.org/en/master/reference/commands.html
---
# The command system
<!-- Better help system -->

Unreal Engine 4 has some built-in commands to help game development. These commands can be typed into a built-in console. Using these commands, a developer can profile the game performance and view debug information.  To invoke the built-in console of a game, type the <code>&#96;</code> key (the key above tab).

<img src="/images/keyboard.png" width="100" alt="Key to invoke console">

UnrealCV adds a set of commands useful for computer vision research. What is more, these UnrealCV commands can be used by an external program.


# Command cheatsheet

<blockquote class='bg-warning'>
  This command list is growing and subject to change<br>
</blockquote>


[Contact us](/contact.html) to tell us what missing functions are useful for your project. We will consider to add it in the future release. This page is generated from UnrealCV automatically. To see the update-to-date help message.
Use {% include script.html key="ls.py" %} to generate the table below.

<!-- how to generate a tree -->

| URI                                                  | Description                                                |
|:-----------------------------------------------------|:-----------------------------------------------------------|
| vget /objects                                        | Get the name of all objects                                |
| vget /object/[obj_name]/color                        | Get the labeling color of an object (used in object instance mask)   |
| vset /object/[obj_name]/color [r] [g] [b]            | Set the labeling color of an object                        |
| vget /camera/[id]/location                           | Get camera location [x, y, z]                              |
| vget /camera/[id]/rotation                           | Get camera rotation [pitch, yaw, roll]                     |
| vset /camera/[id]/location [x] [y] [z]               | Set camera location [x, y, z]                              |
| vset /camera/[id]/rotation [pitch] [yaw] [roll]      | Set camera rotation [pitch, yaw, roll]                     |
| vget /camera/[id]/[viewmode]                         | Get [viewmode] from the [id] camera, for example: vget /camera/0/depth  |
| vget /camera/[id]/[viewmode] [filename]              | Same as the above, with an extra parameter for filename    |
| vset /viewmode [viewmode]                            | Set ViewMode to (lit, normal, depth, object_mask)          |
| vget /viewmode                                       | Get current ViewMode                                       |
| vget /unrealcv/status                                | Get the status of UnrealCV plugin                          |
| vget /unrealcv/help                                  | List all available commands and their help message         |
