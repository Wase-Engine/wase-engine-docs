The Button [Component](Component) draws a interactive button on the screen.

## Methods
| Name | Arguments | Returns | Description |
|-------|---|---|---|
| Button | char* text, [Size](Size), char* font, [TextAlignment](TextAlignment), SDL_Color textColor, SDL_Color buttonColor | | Constructor |
| setButtonPressEffect | bool buttonPressEffect | void | Enable or disable the press effects |
| setButtonHoverEffect | bool buttonHoverEffect | void | Enable or disable the hover effects |
| setButtonColor | SDL_Color color | void | Set the button color |
| setButtonHoverColor | SDL_Color color | void | Set the color for the hover effect |
| setButtonPressColor | SDL_Color color | void | Set the color for the press effect |
| setText | char* text | void | Set the text |
| setTextAlignment | [TextAlignment](TextAlignment) textAlignment | void | Set the text alignment |
| setFont | char* font | void | Set the font |
| setTextColor | SDL_Color color | void | Set the text color |
| setTextHoverColor | SDL_Color color | void | Set the color for the hover effect |
| setTextPressColor | SDL_Color color | void | Set the color for the press effect |
| getTextSize | | [Size](Size) | Get the text size |
| onMouseEnter | | bool | Triggers true if the mouse enters the button |
| onMouseExit | | bool | Triggers true if the mouse exits the button |
| onMouseHold | int button | bool | Returns true if the mouse button is being held down on the button |
| onMouseHover | | bool | Returns true if the mouse hovers over the button |
| onMouseDown | int button | bool | Triggers true if the mouse button is pressed down on the button |
| onMouseUp | int button | bool | Triggers true if the mouse button is released on the button |