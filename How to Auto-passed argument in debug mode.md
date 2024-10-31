# How to Auto-pass argument in Debug mode in vs code

this guides about Using vocodes Workplace settings, custom debugs as way to save time



## Edit `Loanch.json`  -ing

1. Open `launch.json` (ctrl+shift+p)
2. add theses 
``` json
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "type": "autohotkey",
            "request": "launch",
            "name": "Debug with debuging agrument",
            "program": "${file}",
            "args": ["debug"]
        }
    ]
}
```
### Argument -ing:

- you can add more argument in `args` field, search on google if you want more complex
	- arguments without value : `"args": ["arg1", "arg2", "arg3"]`
	- argument with value (not tested) :  `"args": ["--arg1", "value1", "--arg2", "value2"]`
### Name -ing : 

- you can name your custom debug in `name` field 
## Test the Our customized launcher 

this steps to make sure your `launch.json` is being written right 

1. make script copy paste them and save as `AHK` file, then run the new debug mode

``` ahkv2

if A_Args.Length > 0{
    MsgBox "passed with agruments"
    for parm in A_Args  ; For each parameter:
        {   
            if parm ~= "i)debug"{
                ; SC_NSTD_debug := true
                MsgBox "yes debug agrument is enabled"
                global isDebugEnabled := true
                break
            }
        }
    

}{
    MsgBox "didn't passed with agruments"
}


if isDebugEnabled == false {
    MsgBox "debug agrument not enabled"
}
```



## Run Our debugers 

1. ![[attachments/Pasted image 20241031161340.png]]

2. ![[attachments/Pasted image 20241031161353.png]]

   

## `[Opt => speed up]` Custom shortcut for Our new Customized debuggers

1. install this addon https://marketplace.visualstudio.com/items?itemName=ArturoDent.launch-config
2. 

## Thanks and sources

- https://stackoverflow.com/questions/57889703/in-visual-studio-code-how-to-pass-arguments-in-launch-json
- https://stackoverflow.com/questions/48645098/vscode-keyboard-shortcut-for-launch-configuration