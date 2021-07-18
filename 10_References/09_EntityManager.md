Each [Scene](Scene) has a EntityManager that handles all the [Entity](Entity) objects in the [Scene](Scene).

## Properties
| Name | Datatype | Description |
|-------|---|---|
| camera | [Camera](Camera) | The camera |

## Methods
| Name | Arguments | Returns | Description |
|-------|---|---|---|
| addEntity | string name | [Entity](Entity)* | Add an [Entity](Entity) to the scene |
| getEntity | string name | [Entity](Entity)* | Get an [Entity](Entity) by name |

## Usage
```
void TestScene::start()
{
    Entity* entity = entityManager.addEntity("Player");
}
```