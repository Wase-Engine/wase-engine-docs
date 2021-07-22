The Label [Component](Component) draws text on the screen.

## Methods
| Name | Arguments | Returns | Description |
|-------|---|---|---|
| Label | char* text,  char* font, SDL_Color color | | Constructor |
| setText | string text | void | Set the text |
| setFont | char* font | void | Set the font by name from the [ResourceManager](ResourceManager) |
| setColor | SDL_Color color | void | Set the color |
| getSize | | Size | Returns the width and height of the label |