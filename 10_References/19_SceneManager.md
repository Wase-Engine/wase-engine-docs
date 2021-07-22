The SceneManager manages all the scenes.

## Methods
| Name | Arguments | Returns | Description |
|-------|---|---|---|
| addScene | string name, shared_ptr<[Scene](Scene)> scene | void | Load in and store a [Scene](Scene) |
| getActiveScene | | [Scene](Scene)* | Get the active [Scene](Scene) |
| setActiveScene | string name | void | Set the active [Scene](Scene) |