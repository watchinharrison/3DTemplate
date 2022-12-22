# Experience

- [**Utils**](Utils)
- [**World**](World)

### Camera.js

This class sets up perspective and orthographic cameras for use in the scene. There are various helpers that can be enabled in order to better manage camera locations and movement

### Experience.js

This is the singleton Class that will act as the manager for the scene, camera, lighting, controls etc

### Preloader.js

This is where you would define any opening animations prior to any interactions from the user
### Renderer.js

Setting up the WebGL renderer and hooking into the update method for rendering the scene

### Theme.js

Useful for managing themes (including dark/light mode) and emitting the event to be listened on where useful