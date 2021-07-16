To set up a window with Wase Engine you will need to initialize Wase Engine, load in scenes and run it.

*main.cpp*
```c++
#include "example_scene.h"
#include <wase/core/engine.h>
#include <wase/core/managers/scene_manager.h>
#include <memory>

int main(int argc, char* argv[])
{
    // Initialize the engine, specify a title, the window position, the window size and additionally window flags 
    Engine::getInstance()->init("Window title", SDL_WINDOWPOS_CENTERED, SDL_WINDOWPOS_CENTERED, 800, 600, NULL);
    
    // Load in the ExampleScene
    SceneManager::addScene("example", std::make_shared<ExampleScene>());
    
    // Run the engine and let it open the window
    Engine::getInstance()->run("example");

    return 0;
}
```

*example_scene.h*
```c++
#pragma once

#include <wase/core/scene.h>
#include <wase/core/utils/log_utils.h>

class ExampleScene : public Scene
{
public:
    void start()
    {
        log_utils::info("The example scene is now loaded.");
    }
};
```

When you compile and run this code it will open up a 800x600px window with the title 'Window title' and show a log in the console that the example scene has been loaded. This is the minimum you need to set up Wase Engine and open up a window.