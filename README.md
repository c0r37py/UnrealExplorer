# UnrealExplorer
A Private Advanced tool for [Researching, Reversing, UnCooking] Unreal Engine Game Files

#### Developed by: [c0r37py]  -- [Discord](https://discord.gg/uqjmZ5sE2k)
#### Inspired by: [zeroKilo] -- [Project](https://github.com/zeroKilo/PUBGLiteExplorerWV)

## UnrealExplorer - A Mini Unreal Engine Archive Explorer
UnrealExplorer is a powerful and intuitive private C++ application crafted with Qt to dive deep into the heart of Unreal Engine archive files (like .pak files) from packaged games. Think of it as your personal portal into the Unreal Engine ecosystem, running a  lightweight, custom-built mini Unreal Engine to parse, explore, and interact with game assets in a way that feels almost magical. Whether you're a modder, a game developer, or just a curious tinkerer, UnrealExplorer is your ticket to unlocking the secrets of Unreal Engine games with style and precision.

## 🌟 Features That Shine
Asset Browser Extraordinaire: Roam through game packages with a sleek, tree-based Asset Browser that makes finding assets feel like a treasure hunt. From textures to blueprints, it’s all at your fingertips.
Object Inspector with Swagger: Peek under the hood of Unreal objects and classes with a detailed Object Inspector. It’s like having X-ray vision for game data, revealing properties, hierarchies, and more.
Package Parsing Powerhouse: Effortlessly load and dissect .pak files with a custom archive parser, complete with support for asset registries and object resources. It’s like giving your app a PhD in Unreal Engine file formats.
Mini Unreal Engine Vibes: Powered by a lightweight, in-house Unreal Engine-inspired core, UnrealExplorer mimics the real deal with modules for core objects, runtime archives, and editor frameworks. It’s Unreal, but bite-sized!
Gorgeous, Modular UI: Built with Qt’s flexible UI system, the app sports a polished interface with tree views, list views, and detail panels, all styled with a customizable stylesheet (DefaultStyle.qss) for that extra flair.
Developer-Friendly Structure: Organized into modular directories (Core, Runtime, Editor) for easy extension, whether you’re adding new widgets or tweaking the engine’s guts.
Configurability Galore: Fine-tune your experience with settings stored in EditorSettings.ini and ProjectSettings.ini, giving you control over how you explore.

## 🚀 Why UnrealExplorer?
UnrealExplorer isn’t just a tool—it’s a love letter to Unreal Engine enthusiasts. Built from the ground up with Qt 6.9.3 and MSVC 2022 (x64), it’s optimized for Windows and designed to feel snappy yet robust. Whether you’re reverse-engineering game assets, prototyping mods, or just geeking out over Unreal’s inner workings, this app delivers a seamless experience with a touch of elegance. The codebase is clean, the UI is inviting, and the possibilities are endless.

## 🛠️ Getting Started
Clone the Repo: Grab the code and dive into the Source/UnrealExplorer directory to explore the magic.
Build It: Use Visual Studio 2022 with Qt 6.9.3 (MSVC 2022 x64) to compile. The Build folder is ready for your binaries.
Explore Away: Load a .pak file, fire up the Asset Browser, and let the Object Inspector reveal the game’s secrets.
Customize: Tweak styles in Content/Editor/Styles/DefaultStyle.qss or add your own widgets to the Editor/UI folder.

## 💡 Who’s It For?
Modders: Extract and analyze game assets with ease.
Developers: Study Unreal Engine’s file formats or prototype your own tools.
Enthusiasts: Peek into the tech behind your favorite Unreal-powered games.

## 📂 Project Structure
Source/: The heart of the app, with Core (engine fundamentals), Runtime (archive handling), and Editor (UI and tools).
Content/Editor/: Home to icons, shaders, styles, and Qt resource files (EditorResources.qrc).
Config/: Settings files (EditorSettings.ini, ProjectSettings.ini) for personalized exploration.
Build/: Where your compiled dreams come to life.

### Source Structure
```
Source
	│   UnrealExplorer.sln
	│   UnrealExplorer.vcxproj
	│   UnrealExplorer.vcxproj.filters
	│   UnrealExplorer.vcxproj.user
	│
	├───Config
	│       AssetRegistry.ini
	│       Compression.ini
	│       Editor.ini
	│       Uncooking.ini
	│
	├───Content
	│   └───Editor
	│       ├───Resources
	│       │   │   MainWindow.qrc
	│       │   │   UnrealExplorer.rc
	│       │   │
	│       │   └───Icons
	│       │           UnrealExplorer.ico
	│       │
	│       ├───Shaders
	│       └───Styles
	│               DefaultStyle.qss
	│
	└───Source
		│   main.cpp
		│
		└───UnrealExplorer
			├───Core
			│   │   CoreMacros.h
			│   │   CoreMinimal.h
			│   │
			│   ├───Application
			│   │       UEApplication.cpp
			│   │       UEApplication.h
			│   │
			│   ├───Objects
			│   │       UClass.cpp
			│   │       UClass.h
			│   │       UObject.cpp
			│   │       UObject.h
			│   │
			│   ├───Types
			│   │       FName.cpp
			│   │       FName.h
			│   │       FString.cpp
			│   │       FString.h
			│   │       TArray.h
			│   │       TMap.h
			│   │
			│   └───Utilities
			│           FileUtils.cpp
			│           FileUtils.h
			│           StringUtils.cpp
			│           StringUtils.h
			│
			├───Editor
			│   ├───Commands
			│   │       FileCommands.cpp
			│   │       FileCommands.h
			│   │
			│   ├───Dialogs
			│   │       AboutDialog.cpp
			│   │       AboutDialog.h
			│   │       ExportDialog.cpp
			│   │       ExportDialog.h
			│   │       ExportSettingsDialog.cpp
			│   │       ExportSettingsDialog.h
			│   │       ImportDialog.cpp
			│   │       ImportDialog.h
			│   │       SettingsDialog.cpp
			│   │       SettingsDialog.h
			│   │       UncookingDialog.cpp
			│   │       UncookingDialog.h
			│   │
			│   ├───Framework
			│   │       ApplicationCore.cpp
			│   │       ApplicationCore.h
			│   │       MainWindow.cpp
			│   │       MainWindow.h
			│   │
			│   ├───Models
			│   │       AssetTreeModel.cpp
			│   │       AssetTreeModel.h
			│   │       FileSystemModel.cpp
			│   │       FileSystemModel.h
			│   │       ObjectListModel.cpp
			│   │       ObjectListModel.h
			│   │
			│   ├───UI
			│   │       AboutDialog.ui
			│   │       AssetBrowser.ui
			│   │       ExportDialog.ui
			│   │       ExportSettingsDialog.ui
			│   │       ImportDialog.ui
			│   │       MainWindow.ui
			│   │       ObjectInspector.ui
			│   │       PackageViewer.ui
			│   │       PreferencesDialog.ui
			│   │       SettingsDialog.ui
			│   │       UncookingDialog.ui
			│   │
			│   ├───Views
			│   │       DetailsView.cpp
			│   │       DetailsView.h
			│   │       ListView.cpp
			│   │       ListView.h
			│   │       TreeView.cpp
			│   │       TreeView.h
			│   │
			│   └───Widgets
			│           AssetBrowser.cpp
			│           AssetBrowser.h
			│           ObjectInspector.cpp
			│           ObjectInspector.h
			│           PackageViewer.cpp
			│           PackageViewer.h
			│
			└───Runtime
				├───Archieves
				│       AssetRegistry.cpp
				│       AssetRegistry.h
				│       FArchive.cpp
				│       FArchive.h
				│       PakFile.cpp
				│       PakFile.h
				│
				├───Assets
				│       AnimationAsset.cpp
				│       AnimationAsset.h
				│       BlueprintAsset.cpp
				│       BlueprintAsset.h
				│       MaterialAsset.cpp
				│       MaterialAsset.h
				│       SkeletalMeshAsset.cpp
				│       SkeletalMeshAsset.h
				│       SoundAsset.cpp
				│       SoundAsset.h
				│       StaticMeshAsset.cpp
				│       StaticMeshAsset.h
				│       TextureAsset.cpp
				│       TextureAsset.h
				│       WorldAsset.cpp
				│       WorldAsset.h
				│
				├───Compression
				│       OodleCompression.cpp
				│       OodleCompression.h
				│       ZlibCompression.cpp
				│       ZlibCompression.h
				│
				├───CoreUObject
				│       ObjectResource.cpp
				│       ObjectResource.h
				│       Package.cpp
				│       Package.h
				│
				├───Engine
				│       AssetRegistry.cpp
				│       AssetRegistry.h
				│       ImportTable.cpp
				│       ImportTable.h
				│       NameTable.cpp
				│       NameTable.h
				│
				├───Exporters
				│       AnimationExporter.cpp
				│       AnimationExporter.h
				│       AudioExporter.cpp
				│       AudioExporter.h
				│       BlueprintExporter.cpp
				│       BlueprintExporter.h
				│       MaterialExporter.cpp
				│       MaterialExporter.h
				│       MeshExporter.cpp
				│       MeshExporter.h
				│       TextureExporter.cpp
				│       TextureExporter.h
				│
				├───Platforms
				│       PlatformData.cpp
				│       PlatformData.h
				│       PS4Platform.cpp
				│       PS4Platform.h
				│       PS5Platform.cpp
				│       PS5Platform.h
				│       SwitchPlatform.cpp
				│       SwitchPlatform.h
				│       WindowsPlatform.cpp
				│       WindowsPlatform.h
				│       XboxOnePlatform.cpp
				│       XboxOnePlatform.h
				│
				├───Serialization
				│       BinaryReader.cpp
				│       BinaryReader.h
				│       ObjectSerialization.cpp
				│       ObjectSerialization.h
				│       PropertySerialization.cpp
				│       PropertySerialization.h
				│
				├───Shaders
				│       HLSLGenerator.cpp
				│       HLSLGenerator.h
				│       MaterialGraph.cpp
				│       MaterialGraph.h
				│       ShaderDecoder.cpp
				│       ShaderDecoder.h
				│
				└───Uncooking
						AssetUncooker.cpp
						AssetUncooker.h
						Uncooker.cpp
						Uncooker.h
						UncookingSettings.cpp
						UncookingSettings.h
```
UnrealExplorer is more than a parser—it’s a playground for creativity and discovery. Join the adventure and uncover the artistry of Unreal Engine games!
