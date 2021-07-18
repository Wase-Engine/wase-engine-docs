An entity is a object that can be created in a [Scene](Scene). The entities give life to the game because you can interact with them.

## Properties
| Name | Datatype | Description |
|-------|---|---|
| entityManager | [EntityManager](EntityManager)* | The [EntityManager](EntityManager) this entity belongs to |
| parent | Entity* | The parent entity |
| children | vector<Entity*> | The children entities |

## Methods
| Name | Arguments | Returns | Description |
|-------|---|---|---|
| Entity | string name |  | Constructor |
| setParent | Entity* entity | void | Set a parent |
| addComponent | [Component](Component) arguments | T* | Add a [Component](Component) |
| getComponent | | T* | Get a [Component](Component) |
| hasComponent | | bool | Returns if the entity has a certain [Component](Component) |

## Usage
```
void TestScene::start()
{
    Entity* firstEntity = entityManager.addEntity("First entity");
    Entity* secondEntity = entityManager.addEntity("Second entity");
    
    secondEntity.setParent(firstEntity);
    
    firstEntity.getComponent<Transform>()->setPosition(200, 200);
    firstEntity.addComponent<SpriteRenderer>("Cube", 32, 32);
}
```