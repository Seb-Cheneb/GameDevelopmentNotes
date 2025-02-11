[[index|go back]]

# events

---

## parent

Declaring an event:

```csharp
[Signal]
public delegate void SomeEventHandler();
```

Emitting the event:

```
public void Emitter()
{
	EmitSignal(nameof(Some));
}
```

## child

Subscribe to the event:

- usually done in the Ready virtual method
- in case the return signature doesn't match the one of the event handler you can subscribe using anonymous methods

```csharp
Some += Receiver

// using an anonymous method
Some += () => { /* do smth */ }
```

Counterpart method:

- the return type has to be the same as the EventHandler

```csharp
public void Receiver()
{
	// do smth
}
```
