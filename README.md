# libget
A tool where you can use to download the missing libraries for B4A or B4J projects

## How to use
1. Compile the source or download libget.jar from releases to B4X Additional Library folder.
2. Create a libs.json file inside your project's folder (same level as .b4a or .b4j file)
3. In Main module (or B4XMainPage), add the following #Macro tag to the top of the code:\
   Note: Second parameter is ForceUpdate (Boolean)
```B4X
#Macro: Title, GetLibraries, ide://run?file=%JAVABIN%\java.exe&Args=-jar&Args=%ADDITIONAL%\..\B4X\libget.jar&Args=%PROJECT%&Args=True
```
4. Click the AddLibs Macro on the IDE title bar to execute the action.

## Sample libs.json file
```json
{
    "Libraries": [
        {
            "Name": "MiniORMUtils.b4xlib",
            "Platform": "B4X",
            "Version": 2.62,
            "Link": "https://github.com/pyhoon/MiniORMUtils-B4X/releases/download/v2.62/MiniORMUtils.b4xlib"
        },
        {
            "Name": "WebApiUtils.b4xlib",
            "Platform": "B4J",
            "Version": 3.05,
            "Link": "https://github.com/pyhoon/WebApiUtils-B4J/releases/download/v3.05/WebApiUtils.b4xlib"
        }        
    ]
}
```
