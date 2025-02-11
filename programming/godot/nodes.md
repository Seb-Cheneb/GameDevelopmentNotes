[[index|go back]]
# nodes
---
Getting a node from the current tree:
```csharp
_node = GetNode<Node>("Node1/Node2/TheNodeYouNeed");
```

Getting a node from the current tree that has an unique name
```csharp
_node = GetNode<Node>("%TheNodeYouNeed");
```

## getting the parent node of a scene
Getting the parent node
```csharp
private Player _player;

public override void _Ready()
{
	_player = GetParent<Player>();
}
```

## getting nodes in a group
```csharp
Player = GetTree().GetFirstNodeInGroup("PlayerGroup") as Player;
```