## About this fork
It seems like the issue with corrupted blueprint parenting is still there for UE5 projects.
At least I had this problem, and I could not find any other solution nor use [original tool](https://github.com/PipeRift/BlueprintRetarget) release. 
So I recompiled binaries to UE5 (following [this](https://youtu.be/sC0gnfYzFzU?si=5uf0cbu_aO0SIs9G) guide) and publishing it as the fork for those who might still facing the issue.

# Blueprint Retarget plugin
An small tool that allows retargeting invalid blueprints when its parent class is missing

## How to Install
- Go to [release](https://github.com/Islamantin/BlueprintRetarget/releases) section
- Download bin archive of the latest release
- Extract and move the contents to the 'Plugin' folder (e.g. `C:\Program Files\Epic Games\UE_5.1\Engine\Plugins\`)
- Add plugin in UE settings and reload editor

## When to Use
Use this tool when a blueprint has a missing parent class (and therefore you can't open it).

This can happen when:
- It's parent C++ class has been renamed, changed its module or is missing for any other reason.
- It's parent Blueprint class has been lost but still exists somewhere.

Only retarget classes with their original, not modified, parent classes.

### This is not a magic fix button

It won't fix references and blueprints could still fail if the parent has changed or if anything else is corrupted.

**Use it only when the parent class is missing.**

## Usage

1. When having an invalid blueprint, right click on it to see *"Retarget invalid parent"*

<img width=200 src="Content/Readme/ContextMenu.png" /> 

2. After this, a warning will pop up... to warn you

<img width=400 src="Content/Readme/Warning.png" />

3. Finally, select the missing parent from the list. The blueprint will be reparented and you should be able to use it again.
<img width=400 src="Content/Readme/SelectClass.png" />
