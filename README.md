<p align="center">
  <img src="https://raw.githubusercontent.com/Nif-kun/feel-vibes-web-player/main/index.144x144.png">
</p>

# FeelVibes - Editor
An `.fvd` file player made in [FeelVibes - Editor](https://nif-kun.github.io/feel-vibes-web-editor/). The [player](https://nif-kun.github.io/feel-vibes-web-player/) can be embedded to sites and interacted with the following functions below.

### Functions:
Function          | Parameter   | Description
------------------|-------------|------------
getProjectFile    | n/a         | The function can be called to open a file selection dialog, speficially for `fvd` files.
setPlayerDesign   | file (.fvd) | Sets the player design based on the given argument. The file must be an `fvd` for it to work.
resetPlayerDesign | n/a         | Removes any changes in the player, such as design and data stored.
startPlayerDesign | n/a         | Starts the player design animation.
stopPlayerDesign  | n/a         | Stops the player design animation.

### Variables:
Function          | Type   | Description
------------------|--------|------------
projectFile       | blob   | Initially, this will have no value (`null`). Using `getProjectFile()` and selecting an `fvd` file will store the value as a blob type.

#### Example: 
*This can be done in console for testing. However, it must be copy-pasted one by one.*
```
getProjectFile()
setPlayerDesign(projectFile)
startPlayerDesign()

// Call the functions below once you have done the ones above to see changes.
stopPlayerDesign()
resetPlayerDesign()
```

</br>
</br>
</br>

[![Powered by Godot](https://raw.githubusercontent.com/Nif-kun/Nif-kun/main/made-with-godot-small.png)](https://godotengine.org)
