The Transform component handles the position of an [Entity](Entity).

## Properties
| Name | Datatype | Description |
|-------|---|---|
| position | [Vector2](Vector2) | The position |
| depth | int | The depth is used to determine which sprite gets rendered in front |

## Methods
| Name | Arguments | Returns | Description |
|-------|---|---|---|
| Transform | float x(additional), float y(additional), int depth(additional)  |  | Constructor |
| setPosition | float x, float y | void | Set a position |