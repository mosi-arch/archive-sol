# Library Information

- just import library OR write in same file like this example
- type 1: library.function(arguments)
- type 2: using library for type; 
- - type as frist arg: type.function(other arguments);

this is an example for *writing* and *using* ***libraries***

> 18 august 2022

### type 1 example
```solidity
Calls.callIn(address(this), msg.value);
```

### type 2 example
```solidity
using Calls for address;

msg.sender.callOut(value);
```
