The SpriteRenderer can be used to render images/sprites on the screen.

## Properties
| Name | Datatype | Description |
|-------|---|---|
| color | SDL_Color | The color of the sprite |
| rect | SDL_Rect | Contains the position and dimensions of the SpriteRenderer |

## Methods
| Name | Arguments | Returns | Description |
|-------|---|---|---|
| SpriteRenderer | string name, int sizeX, int sizeY |  | Constructor |

## Usage
```
void TestScene::start()
{
    Entity* entity = entityManager.addEntity("Player");
    
    // The first argument references to the ResourceManager texture name, the second and third argument are the width and height of 1 frame of a spritesheet
    entity->addComponent<SpriteRenderer>("Player", 32, 32);
}
```