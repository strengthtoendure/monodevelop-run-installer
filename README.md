# MonoDevelop has returned to providing per distro packages, this repo will no longer be maintained.

# A simple .run installer for MonoDevelop 

This is a simple .run installer for the newest version of MonoDevelop. I created this since the flatpak version is still quite unstable (flatpak version sandboxes the app which hides the system folders from it, this makes debugging stuff which requires system libraries impossible since they can't load system libs, and there are also problems with using MonoGame for example which is depandand on the content builder, which gets installed in /usr).

## Installing

To install simply download a release and do:
```
chmod +x monodevelop-{version}.run
sudo ./monodevelop-{version}.run
```
where you replace `{version}` with the version you've downloaded. The installer will not download dependencies (mono, xbuild, etc.) so you should install `monodevelop` package from you systems default repos to fetch them quickly.

The installer will add "MonoDevelop Stable" application launcher, as well as the following commands:
 - monodevelop-stable - Launches MonoDevelop
 - mdtool-stable - Launches MDTool
 - monodevelop-stable-uninstall - Uninstalls MonoDevelop from .run installer

## Building installer from source

To build from source, simply download and install `flatpak`, and after than just call the generate script (it will automatically download and update MonoDevelop for you):
```
./generate.sh
```
