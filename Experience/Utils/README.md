# Utils

### assets.js 

List your assets and relative paths to be loaded by the Resources Util
    
### Resources.js

This util class will setup loaders for GTLF, DRACO compression and then begins loading assets and assigning them to items

### Sizes.js

This util sets up window dimensions, helper device variables and listens on window resize, emitting a resize event that can be listened on

### Time.js

This util sets up some helper variables and hooks up the request animation frame to the update method. This method then emits an update event that can be used by the Experience to sync up the dependent update methods (camera, renderer etc)


