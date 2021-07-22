In Wase Engine you have the possibility to have multiple scenes and switch between them. All the scenes must be loaded in before the run method gets called.

## Loading scenes
*main.cpp*
```
#include <wase/core/engine.h>
#include <wase/core/managers/scene_manager.h>
#include <memory>

using namespace wase;

int main(int argc, char* argv[])
{
    // Initialize the engine, specify a title, the window position, the window size and additionally window flags 
    Engine::getInstance()->init("Window title", SDL_WINDOWPOS_CENTERED, SDL_WINDOWPOS_CENTERED, 800, 600, NULL);
    
    // Load in the ExampleScene
    SceneManager::addScene("Main Menu", std::make_shared<MainMenu>());
    SceneManager::addScene("Settings menu", std::make_shared<Settings>());
    SceneManager::addScene("Game", std::make_shared<Game>());
    
    // Run the engine and let it open the window
    Engine::getInstance()->run("Main Menu");

    return 0;
}
```

As you can see the SceneManager class takes care of all the scene's. First you load in all the scenes and after that you can run Wase Engine. In the run method you'll have to specify which scene has to be loaded first.

## Switching between scenes
The SceneManager offers the ability to switch  between scenes during runtime. You can call the method setActiveScene everywhere.
```
// The Main Menu scene gets called every frame
void MainMenu::update(float dt)
{
    // If space is pressed
	if (input::getKeyDown(SDLK_SPACE))
	{
	    // Change the scene to the Game scene
		SceneManager::setActiveScene("Game");
	}
}
```

## Getting the current scene
To get the current scene you can call:
```
SceneManager::getActiveScene()
```