# godot-bug-scene-conflict
An example project to show an issue in godot 2.1.4
If scene is changed externally while open in godot, no prompt is given of this conflict.
This is a nuisance when working with a team on a project, when for instance git pulling while godot is open, without realizing the conflict, then overwriting the changes.

# How to setup
1 Clone project.
2 Open godot 2.1.4
3 Import project from cloned folder.
4 Open the scene file called 'scene.tscn'
While you have the scene open in godot do next either 4a or 4b
4a open a terminal and run the shell script 'change.sh' -it replaces scene.tscn with new_scene.tscn
4b open a terminal and type git checkout new-scene
5 go into godot and notice that no prompt is given, despite the currently open scene has been externally modified.
if you close the scene and reopen it, you will see the new modified scene with its new changes.
if you dont, and continue working, you will, when you decide to save, overwrite the external modifications.

