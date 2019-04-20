## SketchUnlimited
SketchUnlimited is an OSX application that run Sketch without considering the trial expired. 

The way to trick Sketch.app is by modifying the system time before the trial date started, and correct the time after the application start.

You can use the `compile` script to build an application from the AppleScript:
```Shell
./compile
```

Or you can copy the code from `SketchUnlimited.applescript` to Automator by creating action `Run AppleScript` and export to `/Applications`.

**SketchUnlimited.applescript**
```AppleScript
do shell script "date 0420080019 && open /Applications/Sketch.app && sntp -sS time.apple.com" with administrator privileges
```

![SketchUnlimited Automator](https://user-images.githubusercontent.com/32001663/56462192-f52bd900-63b6-11e9-8228-5444a90711f2.png)

Once you launch the `SketchUnlimited`, it needs the permission to change the system and open `Sketch.app` in `/Applications`. 
![Permission Request](https://user-images.githubusercontent.com/32001663/56462244-dbd75c80-63b7-11e9-9081-8d51db9493d0.png)

After entering `Username` and `Password`, you can use `Sketch` without trial limited. Enjoy it!
![Sketch Launched](https://user-images.githubusercontent.com/32001663/56462260-32449b00-63b8-11e9-84d8-0e34863c1e2c.png)


### Reference:
* [Bhavdip/sketch-never-ending](https://gist.github.com/Bhavdip/76c581d7ac03bdce6d226a2e8c522df4)
* [AlexeySemigradsky Sketch Runner](https://github.com/AlexeySemigradsky/SketchRunner)