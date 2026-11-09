# GDExtensionsPlayGround
This is where I post all my custom GDExtensions that wouldn't need a whole repository just for it!

## Building on macOS

Requires the Xcode command line tools and SCons.

1. Clone the Godot C++ bindings next to the extension folders:
   ```
   git clone --branch godot-4.5-stable https://github.com/godotengine/godot-cpp.git godot-cpp
   ```
2. Build each extension from its folder:
   ```
   cd MiniAudioMic   # or CustomMeshDeform
   scons platform=macos build=debug
   scons platform=macos build=release
   ```

The first build also compiles godot-cpp. The libraries are universal (arm64 + x86_64) and are written to `bin/macos/`.
