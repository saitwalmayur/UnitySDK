# Unity Native Toast Plugin (Android)

A lightweight Unity package that allows you to display **native Android Toast messages** from Unity using a simple C# API.  
Delivered as a **UnityPackage** for easy import into any Unity Android project.

---

## 📦 Package Contents

This `.unitypackage` includes:

Assets/
└── NativeToast/
├── Example/
│ └── Toast/
│ ├── DetectClick.cs
│ └── ToastExample.prefab
├── Plugins/
│ ├── Android/
│ │ └── unityandroidplugin.aar
│ └── Scripts/
│ └── NativeSdk.cs

---

## 🚀 Getting Started

### 1. Import the Unity Package

In Unity:

Assets → Import Package → Custom Package…

---

### 2. Open the Example

Go to:

Assets/NativeToast/Example/Toast/

### This example contains:
- Cube  
- Sphere  
- Cylinder  
- Capsule  

Each object has `DetectClick.cs` attached.

### What happens?

👉 When you **tap any object** on your Android device,  
Unity calls:

NativeSdk.Instance.ShowLongToast(gameObject.name);

So you will see a toast like taped object names
🧠 Usage (In Your Game)

You can show toast from ANY script:

NativeSdk.Instance.ShowShortToast("Hello from Unity!");
NativeSdk.Instance.ShowLongToast("This is a long toast!");


🚀 No Prefabs Needed

You do not need to create any prefabs or place any objects inside the scene manually.
The script uses:

[RuntimeInitializeOnLoadMethod(RuntimeInitializeLoadType.BeforeSceneLoad)]

