# Building

Only needed to change the code. Needs Visual Studio 2022 Build Tools (C++ x86) and a Windows 11 SDK.
Not yet verified from a fresh checkout.

1. `git clone --recursive https://github.com/elishacloud/dxwrapper`, then check out `d77702d5` and run
   `git submodule update --init --recursive`.
2. Apply `source/tpw-changes-to-dxwrapper.patch` in the root.
3. Check out `d352bb9` in `External/Logging` and apply `source/tpw-changes-to-Logging.patch` there.
4. Edit `d3d8/BuildNo.rc` so its only content is `#define FILEVERSION 1.16.0.0` with nothing after it.
   The original build did this by hand.
5. Build MakeShader, then, from an x86 developer prompt, with the checkout's path in `SolutionDir`:

   ```text
   msbuild dxwrapper.vcxproj /p:Configuration=Release /p:Platform=Win32 /p:SolutionDir=<checkout>\ /p:PreBuildEventUseInBuild=false
   ```

Output: `bin\Release\dxwrapper.dll`. A rebuild will not have the release file's hash.
`ddraw.dll` is dxwrapper's loader and is unchanged.
