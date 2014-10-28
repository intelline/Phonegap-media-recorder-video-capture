
New media video capture plugin for phonegap using media recorder
=======


How to install the plugin
-----------

1. Install the plugin with this command 
```
phonegap.cmd plugin add ..\com.phonegap.newmedia```
2. Copy the **MediaRecorderRecipe.java** to the directory of your main activity java file.
3. From the layout folder, copy the xml file to the layout folder of your phonegap project `[project_name]\platforms\android\res\layout\`
4. From the drawable folder, copy the files to the drawable folder of your phonegap project `[project_name]platforms\android\res\drawable\`
5. Use the javascript to start the camera activity view
6. Use the result of the activity(result is the filename) to do what ever you like.

How to use the javascript
-----------

```
// start the camera activity
NewMedia.startRecord(captureSuccess, captureError, {
	"bitrate": 700000,
	"width": 480,
	"height": 360,
});

// capture success callback
function captureSuccess(data) {
	if (data.fullpath !== '') {
		
	}
}

// capture error callback
function captureError(error) {
    console.log("camera failed ", error);
}
```