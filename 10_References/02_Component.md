This class is the base class for all the components.

## Properties
| Name | Datatype | Description |
|-------|---|---|
| owner | [Entity](Entity)* | The entity that the component is attached to |

## Methods
| Name | Arguments | Returns | Description |
|-------|---|---|---|
| start |  | void | Gets run when the component becomes active |
| update | float dt | void | Runs every frame |
| render | | void | Can be used to seperate the rendering code from the other code |
| onStateChange | bool state | void | Gets called when the component its state changes |
| isActive | | bool | Returns if the component is active |
| setActive | bool state | void | Change the component state to active or inactive |