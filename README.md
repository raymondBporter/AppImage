# AppImage

ImageLab, the raster workbench extracted from App2d. Load an image, apply transforms
with undo/redo, repair masks and edges, and export PNGs.

Clone this repository beside an [App2d checkout](https://github.com/raymondBporter/App2d):

```text
source/
  App2d/
  AppImage/
  AppAnimation/
```

Requires Windows and the .NET 10 SDK or newer. Open `AppImage.slnx`, or run:

```powershell
dotnet build AppImage.slnx
dotnet run --project App2d.ImageLab
dotnet test App2d.ImageLab.Tests
```

Core and EditorUi use ordinary project references to the sibling App2d checkout.
For another layout, pass `-p:App2dRoot=C:/path/to/App2d` to the build, run, or test
command. No submodules, copied engine code, or Git setup between repositories.

See [the ImageLab guide](App2d.ImageLab/README.md) for controls, transforms, and UI
smoke commands. Its five raster workbench test files now live in
`App2d.ImageLab.Tests`; Core imaging tests remain in App2d.
