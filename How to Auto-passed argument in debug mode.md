# launch
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
## argument :
- you can add more argument in `args` field, search on google if you want more complex
	- arguments without value : `"args": ["arg1", "arg2", "arg3"]`
	- argument with value (not tested) :  
## Name:
- you can name your custom debug in `name` field 
# test

this steps to make sure your `launch.json` is be written right make script copy paste them and save th, then run debug mode

``` ahk

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
    

}


if isDebugEnabled == false {
    MsgBox "debug agrument not enabled"
}
```

<mark style="background: yellow" >Hello world  </mark>

<mark style="background: #BBFABBA6;">name your custom</mark>

| `$${\color{yellow}Yellow}$$` |      |
| ---------------------------- | ---- |
|                              |      |

sss $${\color{yellow}Yellow}$$ sss

`$${\color{yellow}Yellow}$$`