# FTK Plugin templates

## **Available templates**:

- ftk-plugin - modified bepinex5plugin template pre-configured for correct Unity and .NET Framework version. Contains `prepare.bat` that will fetch stripped binaries as git submodule.

## Installation

**Using dotnet templates**

Each release will contain .nupkg file that can be installed locally using following command:

`dotnet new --install E:\Dev\bepinex\plugin-development\PluginTemplate\bin\Debug\Amadare.FTKPlugin.Templates.1.0.0.nupkg`

after that, you can create projects from template like so:

`dotnet new ftk-plugin -n MyPluginName`

That will create pre-configured plugin solution that will can be used in bepinex without additional configuration.
> IMPORTANT: after project creation, execute `prepare.bat` script. It will download necessary FTK binaries and run `dotnet restore`.

**Using zip file**

If you don't want to install dotnet templates, you can just download zip release and replace all strings "FTKPlugin" to name of your plugin using "search and replace in files" function of your text editor. Note that filenames should be changed as well. Run `prepare.bat` afterwards.