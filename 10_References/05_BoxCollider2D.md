The BoxCollider2D [Component](Component) is build on the [Collider](Collider) class. It is a rectangle shaped [Collider](Collider).

## Properties
| Name | Datatype | Description |
|-------|---|---|
| width | int | The width |
| height | int | The height |
| offset | Vector2 | An additional offset to the [Entity](Entity) position |
| showCollider | bool | A green outline for the [Collider](Collider) |

## Methods
| Name | Arguments | Returns | Description |
|-------|---|---|---|
| BoxCollider2D | int width, int height |  | Constructor |
| onMouseEnter | | bool | Triggers true if the mouse enters the [Collider](Collider) |
| onMouseExit | | bool | Triggers true if the mouse exits the [Collider](Collider) |