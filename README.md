## 3D Experience Template

### Structure

main.js - This is where you will load the experience targeting the canvas html dom target to load the scene into

/public
  /models - This is where you will store any .glb models for loading into the project
  /textures - This is for any image/video textures you will apply to Meshes after loading the model
  /draco - this is an open-source library to handle compressed .glb models

/Experience
  /Utils
    /assets.js - List your assets and relative paths to be loaded by the Resources Util
    /Resources.js - This util class will setup loaders for GTLF, DRACO compression and then begins loading assets and assigning them to items
    /Sizes.js - This util sets up window dimensions, helper device variables and listens on window resize, emitting a resize event that can be listened on
    /Time.js - This util sets up some helper variables and hooks up the request animation frame to the update method. This method then emits an update event that can be used by the Experience to sync up the dependent update methods (camera, renderer etc)
  /World
    /Controls.js - If your experience relies on user input, including scroll, this class registers the plugin ScrollTrigger from gsap and uses the smooth scrolling package from ASScroll. This is useful for translating the users scroll into animating your various model objects.
    /Environment.js - This manages the lighting and theme controls for the Experience. It also includes helpers for tracking lighting in the scene and a GUI to control properties on the Lightening like colour and intensity
    /Floor.js - If your scene requires a horizontal plane to act as a floor this class sets that up.
    /World.js - Inits the environment, world and controls for the experience.
  /Camera.js - This class sets up perspective and orthographic cameras for use in the scene. There are various helpers that can be enabled in order to better manage camera locations and movement
  /Experience.js - This is the singleton Class that will act as the manager for the scene, camera, lighting, controls etc
  /Preloader.js - This is where you would define any opening animations prior to any interactions from the user
  /Renderer.js - Setting up the WebGL renderer and hooking into the update method for rendering the scene
  /Theme.js - Useful for managing themes (including dark/light mode) and emitting the event to be listened on where useful

### Development

