To prevent loading in the same file multiple times there is a ResourceManager, the ResourceManager class can load in and return files so they can be reused.

## Loading resources
*main.cpp*
```c++
#include <wase/core/engine.h>
#include <wase/core/managers/scene_manager.h>
#include <wase/core/managers/resource_manager.h>
#include <memory>

int main(int argc, char* argv[])
{
    // Initialize the engine, specify a title, the window position, the window size and additionally window flags 
    Engine::getInstance()->init("Window title", SDL_WINDOWPOS_CENTERED, SDL_WINDOWPOS_CENTERED, 800, 600, NULL);
    
    // Load in the resources
    ResourceManager::loadTexture("Cube", "assets/sprites/cube.png");
    ResourceManager::loadFont("Opensans", "assets/fonts/opensans.ttf", 20);
    ResourceManager::loadAudio("Music", "assets/music/song.mp3")
    
    // Load in the scenes
    SceneManager::addScene("Game", std::make_shared<Game>());
    
    // Run the engine and let it open the window
    Engine::getInstance()->run("Main Menu");

    return 0;
}
```

The ResourceManager can be used to load in images, fonts and audio files.  Like in the example above you will have to specify a name for the file that will be used to save the file in the ResourceManager and you will have to specify a path relative to the project root. For the loadFont method you will also have to specify a font size.

## Getting resources
To get a resource from the ResourceManager you can call the following methods from everywhere:
```c++
ResourceManager::getTexture("Texture name")
ResourceManager::getFont("Font name");
ResourceManager::getAudio("Audio name");
```