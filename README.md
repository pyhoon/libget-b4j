# libget-non-ui-b4j
a tool where you can use to download the missing libraries for B4A or B4J projects

## How to use
1. Compile the source and rename the jar as libget-non-ui.jar
2. Put the jar into B4X additional libraries folder
3. Create a libs.json file
4. Put the libs.json file inside your project's folder (same level as .b4a or .b4j file)
5. In Main module (or B4XMainPage), add the following comment link to the top of the code:
```
' LibDownloader: ide://run?file=%JAVABIN%\java.exe&Args=-jar&Args=%ADDITIONAL%\..\B4X\libget-non-ui.jar&Args=%PROJECT%
```
6. Mouse hover to the comment link and Ctrl+Click on it

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
