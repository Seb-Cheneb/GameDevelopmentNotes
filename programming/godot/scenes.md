[[index|go back]]
# scenes
---
## defining
### long version
Getting hold of a scene
```csharp
private PackedScene _scene;

public override void _Ready()
{
	_scene = ResourceLoader.Load<PackedScene>("res://Scenes/DamageNumber.tscn");
}
```

Instantiating a scene once it is defined:
```csharp
var newScene = _scene.Instantiate() as Node3D;
```
### short version
```csharp
private Node3D _scene;

public override void _Ready()
{
	_scene = ResourceLoader.Load<PackedScene>("res://Scenes/DamageNumber.tscn") as Node3D;
}
```

Instantiating a scene once it is defined:
```csharp
var newScene = _scene.Instantiate() as Node3D;
```
```
## adding scene to tree

Adding the scene as a child of the current tree:
```csharp
AddChild(newScene);
```