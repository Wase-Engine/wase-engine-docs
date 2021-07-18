The ResourceManager manages all the files. It will prevent that a file will be loaded in twice.

## Methods
| Name | Arguments | Returns | Description |
|-------|---|---|---|
| loadTexture | string name, char* path | void | Load in and store an image file |
| loadAudio | string name, char* path | void | Load in and store an audio file |
| loadFont | string name, char* path | void | Load in and store a font file |
| getTexture | string name | SDL_Texture* | Get a texture by name |
| getAudio | string name | Mix_Chunk* | Get a mix chunk by name |
| getFont | string name | TTF_Font* | Get a font by name |