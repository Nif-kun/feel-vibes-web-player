# feel-vibes-web-player
Official FeelVibes web player.

### Script:
```
var projectFile;
var dataBuffer = {};
var playerDesign;
var resetPlayerDesign;
var startPlayerDesign;
var stopPlayerDesign;

function getProjectFile() {
  window.input = document.createElement('input');
  input.accept = ".fvd"
  input.type = 'file'
  input.click();

  input.onchange = e => {
    projectFile = e.target.files[0];
  }
}

function setCallbacks(setDesignCallback, resetCallback, startCallback, stopCallback ) {
  playerDesign = setDesignCallback;
  resetPlayerDesign = resetCallback;
  startPlayerDesign = startCallback;
  stopPlayerDesign = stopCallback;
}

function setPlayerDesign(file) {
  var reader = new FileReader();
  reader.readAsArrayBuffer(file);
  reader.onloadend = readerEvent => {
    if (readerEvent.target.readyState == FileReader.DONE) {
      dataBuffer.result = readerEvent.target.result;
      playerDesign(file.name);
    }
  }
}
```

### Copy-Paste: 
*Paste one by one.*
```
getProjectFile()
setPlayerDesign(projectFile)
startPlayerDesign()
```
