To log information to the console you can use the logging system of Wase Engine.
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
        log_utils::info("Info");
        log_utils::success("Success");
        log_utils::error("Error");
    }
};
```

You can call the logging methods from everywhere and it accepts any type of arguments.