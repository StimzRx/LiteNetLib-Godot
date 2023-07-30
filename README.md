# LiteNetLib-Godot

Lite reliable UDP library modified for use with the Godot game engine

For full/original documentation please see [The Original GitHub Project](https://github.com/RevenantX/LiteNetLib)

## My Changes
I have pretty much just added the ability to use the GodotSharp Vector structs
with this library. I did this by implementing the following types:
 - ``Godot.Vector2``
 - ``Godot.Vector2I``
 - ``Godot.Vector3``
 - ``Godot.Vector3I``

Inside of both ``NetDataReader.cs`` and ``NetDataWriter.cs``.
More information is as follows:

### NetDataReader
#### Get's:
 - ``Vector2 GetVector2();``
 - ``Vector2I GetVector2I();``
 - ``Vector3 GetVector3();``
 - ``Vector3I GetVector3I();``
#### Peek's
 - ``Vector2 PeekVector2()``
 - ``Vector2I PeekVector2I()``
 - ``Vector3 PeekVector3()``
 - ``Vector3I PeekVector3I()``
#### TryGet's
 - ``bool TryGetVector2(out Vector2 result)``
 - ``bool TryGetVector2I(out Vector2I result)``
 - ``bool TryGetVector3(out Vector3 result)``
 - ``bool TryGetVector3I(out Vector3I result)``

### NetDataWriter
 - ``void Put(Vector2 value)``
 - ``void Put(Vector2I value)``
 - ``void Put(Vector3 value)``
 - ``void Put(Vector3I value)``


**Note:** I mostly did this fork due to growing tired of re-doing these
functions each time I made a new Godot project that used LiteNetLib.
Due to the reliance on the ``GodotSharp.dll`` library that ships with the 
Godot engine, I didnt think it would be reasonable to do a PR to add these
features to the main branch.
