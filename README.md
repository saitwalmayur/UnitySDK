Unity Native Toast Plugin (Android)

A lightweight Unity package that enables you to display native Android Toast messages directly from Unity using an easy C# API.
Delivered as a .unitypackage for plug-and-play integration in any Unity Android project.

📦 Package Contents

This package includes the following folder structure:

Assets/
└── NativeToast/
    ├── Example/
    │   └── Toast/
    │       ├── DetectClick.cs
    │       └── ToastExample.prefab
    ├── Plugins/
    │   ├── Android/
    │   │   └── unityandroidplugin.aar
    │   └── Scripts/
    │       └── NativeSdk.cs

🚀 Getting Started
1. Import the Unity Package

In Unity:

Assets → Import Package → Custom Package…
Select the provided .unitypackage.

▶️ Example Scene

After importing, navigate to:

Assets/NativeToast/Example/Toast/

The example scene contains:

Cube

Sphere

Cylinder

Capsule

Each object has the script DetectClick.cs attached.

✔️ What Happens?

When you tap any of these objects on your Android device, Unity executes:

NativeSdk.Instance.ShowLongToast(gameObject.name);


This displays a toast message showing the tapped object's name.

🧠 Usage in Your Own Game

You can show native toast messages from any script:

NativeSdk.Instance.ShowShortToast("Hello from Unity!");
NativeSdk.Instance.ShowLongToast("This is a long toast!");

🚀 No Prefabs Needed — Auto Initialization

You do not need to:
❌ Create any prefab
❌ Add anything to your scene
❌ Manually initialize the plugin

The SDK script automatically initializes before the first scene loads using:

[RuntimeInitializeOnLoadMethod(RuntimeInitializeLoadType.BeforeSceneLoad)]


This ensures the plugin is ready to use instantly when the game starts.
