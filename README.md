# camera_silence
explains how to remove the camera shutter sound of a cell phone without any app.

## install
Connect your phone to the computer via USB and allow access.

<img src="https://user-images.githubusercontent.com/53033449/88524582-7f400400-d034-11ea-9875-c621bc621ca6.jpg" width="30%"><img src="https://user-images.githubusercontent.com/53033449/88482338-90890200-cf9b-11ea-9949-bc970965617f.jpg" width="30%"><br><br>
Go to the mobile phone information tab and go to the software information tab.
<br>

<img src="https://user-images.githubusercontent.com/53033449/88523865-96cabd00-d033-11ea-9080-0b04705a5019.jpg" width="30%"><img src="https://user-images.githubusercontent.com/53033449/88525315-66841e00-d035-11ea-9543-b0177a77462c.jpg" width="30%"><br><br>
Touch the build number tab multiple times.
<br>
<img src="https://user-images.githubusercontent.com/53033449/88523917-acd87d80-d033-11ea-8d68-4898907323af.jpg" width="30%"><img src="https://user-images.githubusercontent.com/53033449/88523920-ae09aa80-d033-11ea-909d-d346a5a61c2f.jpg" width="30%"><br><br>
Enter the pin number to turns on developer mode.<br>
If you go down of setting menu, you can see developer mode was on.  
<br>
<img src="https://user-images.githubusercontent.com/53033449/88523924-aea24100-d033-11ea-84cc-9d966731a8fe.jpg" width="30%"><img src="https://user-images.githubusercontent.com/53033449/88523931-af3ad780-d033-11ea-8508-77029ac42a46.jpg" width="30%"><br><br>
Enter developer mode, locate and touch USB debugging items.
<br>
<img src="https://user-images.githubusercontent.com/53033449/88523934-b06c0480-d033-11ea-92b9-be59cece2dbe.jpg" width="30%"><br><br>
Touch OK all of items
<br>
<img src="https://user-images.githubusercontent.com/53033449/88523937-b1049b00-d033-11ea-9395-62dd8f57da96.jpg" width="30%"><img src="https://user-images.githubusercontent.com/53033449/88523943-b235c800-d033-11ea-8150-4bd2ac92c087.jpg" width="30%">

<br>

[ADB Download](https://developer.android.com/studio/releases/platform-tools?hl=ko, "ADB Download link")


<img src="https://user-images.githubusercontent.com/53033449/88534891-eadd9d80-d043-11ea-92c2-823a3f4358ce.jpg"><br><br><br>

Unzip the downloaded file and open the PowerShell with Shift + Right-click.
<img src="https://user-images.githubusercontent.com/53033449/88565240-45402380-d06f-11ea-916b-74b77da2c494.jpg"><br><br>

Enter the command below to make your phone's camera silent!
- window
```
.\adb.exe shell settings put system csc_pref_camera_forced_shuttersound_key 0
```
- mac
```
adb shell settings put system csc_pref_camera_forced_shuttersound_key 0
```

- window
If you want it back, enter below command.
```
.\adb.exe shell settings put system csc_pref_camera_forced_shuttersound_key 1
```

- mac
```
adb shell settings put system csc_pref_camera_forced_shuttersound_key 1
```

 ## *if your phone wasn't in silent mode, shutter sound will not remove. Only silent mode can remove shutter sounds*
 
 ### error correction :  _*error: more than one device/emulator*_
 ```
 ./adb kill-server
 ./adb device
 ```
