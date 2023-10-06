# How to organize scenes

1. Create a Node "Main" (main.gd) to be the primary controller.
2. Add World and GUI children nodes:

- Node "Main" (main.gd)
  - Node2D/Node3D "World" (game_world.gd)
  - Control "GUI" (gui.gd)

When changing levels, one can then swap out the children of the "World" node.

References:

- [Godot docs](https://docs.godotengine.org/en/stable/tutorials/best_practices/scene_organization.html)
