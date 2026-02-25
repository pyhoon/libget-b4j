# libget
A tool where you can use to download the missing libraries for B4A or B4J projects

## How to use
1. Compile the source or download libget.jar from releases to B4X Additional Library folder.
2. Create a libs.json file inside your project's folder (same level as .b4a or .b4j file)
3. In Main module (or B4XMainPage), add the following #Macro tag to the top of the code:
```B4X
#Macro: Title, GetLibraries, ide://run?file=%ADDITIONAL%\..\B4X\libget.jar&Args=%PROJECT%&Args=AutoUpdate
```
4. Click the GetLibraries Macro on the IDE title bar to execute the action.

Note: \
First argument is project path containing the libs.json file \
Second argument is option

Available options:
- AutoUpdate
- ForceDowngrade
- CheckOnly 

## Sample libs.json file
```json
{
    "Libraries": [
        {
            "Name": "MiniJS.b4xlib",
            "Platform": "B4X",
            "Version": 0.40,
            "Link": "https://github.com/pyhoon/MiniJs-B4X/releases/download/v0.40/MiniJs.b4xlib",
            "Update": "https://github.com/pyhoon/MiniJs-B4X/releases/download/v0.40/update.json"
        },
        {
            "Name": "WebApiUtils.b4xlib",
            "Platform": "B4J",
            "Version": 5.90,
            "Link": "https://github.com/pyhoon/WebApiUtils-B4J/releases/download/v5.90/WebApiUtils.b4xlib"
        }        
    ]
}
```

## Sample update.json file
```json
{
    "Name": "MiniJS.b4xlib",
    "Platform": "B4X",
    "Version": 0.50,
    "Link": "https://github.com/pyhoon/MiniJs-B4X/releases/download/v0.50/MiniJs.b4xlib"
}
```
