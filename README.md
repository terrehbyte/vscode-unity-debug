# Unity Debugger Extension for Visual Studio Code

This extension is not officially supported by Unity Technologies.

Use Visual Studio Code to debug your Unity C# projects.

## Setup

- Open your Unity project folder in the Visual Studio Code.

- Select the debug view on the left and click the cogwheel.

![Debug View](Screenshots/vscode-debug-view.png)

- In the drop down list select “Unity Debugger”. If you do not have Unity Debugger in the list, then you already have a .vscode/Launch.json file in your project that you must delete first.

![Debugger List](Screenshots/vscode-debugger-list.png)

- You will now have a .vscode/Launch.json file in your Unity project folder and can select which Unity target you wish to debug.

![Debugger List](Screenshots/vscode-debugger-unity.png)

- All done. You can now debug your C# scripts in VS Code by setting a breakpoint in a C# script from your project, switching to the debug view and clicking the green triangle button to attach to Unity. Enter play mode in Unity and the breakpoint should hit in VS code.

## Attach to Process Picker

New in version 1.1.0 it is now possible to select which Unity process you want to attach to from a quick pick menu.

- In the command palette type "Unity Attach Debugger"

- Wait a bit for the Unity processes list to appear at the top of the VS Code window.

- Select the Unity process you wish to attach the debugger to.

## Usage

Strings in the variable view is truncated to 100 characters, with appended ellipsis. "Example wor...". To view the entire value of this string add it to the watch fields. In addition, evaluating the variable using the debugger console will reveal the same result.

## Building

### Dependencies

- Visual Studio
- Visual Studio Code
- NPM

You should have at least a basic understanding of how [VS Code extensions are
developed][vsc-ext] before working on this extension.

### Quick Start

To start building this repository, clone with the `--recursive` parameter to
retrieve all submodules.

```bash
git clone --recursive https://github.com/Unity-Technologies/vscode-unity-debug
```

Open `VSCode-UnityDebug.sln` in Visual Studio and build `UnityDebug`.

If you're missing any targeting packs (ex: .NET Framework 4.7.1), download and
install them as prompted. You'll then want to restart Visual Studio, clean the
solution, and then build the project again. (You'll also follow these steps if
you get "metadata" errors.)

If you haven't already, install "Visual Studio Code Extensions" from NPM.

```bash
npm install -g vsce
```

You should be able to now build the extension and begin developing/debugging it
using Visual Studio Code.

```bash
# install project dependencies
npm install

# package the extension
vsce package
```

Alternatively, you can open the repository in VS Code and use the provided
Debug Task ("Launch Extension") to launch a new instance of VS Code with your
newly built version of this extension.

For more information about working with Visual Studio Code Extensions, see the
[official documentation from Microsoft][vsc-ext].

[vsc-ext]:https://code.visualstudio.com/api
