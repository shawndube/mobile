# Toggl Mobile

This repository contains the source code for building the native Toggl Android and iOS applications.
These applications are build using [Xamarin](http://xamarin.com/) products to allow for maximum
code reuse and faster development times.

## Repository structure

The repository consists of the following projects:

- Phoebe - shared data models and business logic across platforms
- Joey - Android application (UI & Android specific code)
- Ross - iOS application (UI & iOS specific code)
- Tests - unit tests for testing code in Phoebe

Phoebe has several project files ([Phoebe.Android.csproj](https://github.com/toggl/mobile/blob/master/Phoebe/Phoebe.Android.csproj), [Phoebe.iOS.csproj](https://github.com/toggl/mobile/blob/master/Phoebe/Phoebe.iOS.csproj) and [Phoebe.Desktop.csproj](https://github.com/toggl/mobile/blob/master/Phoebe/Phoebe.Desktop.csproj)) which compile the same code for different target platforms
(Android, iOS and desktop).

## Setting up

You should begin by initializing git hooks and submodules:

	$ make setup

You also need to restore NuGet packages for the solution. In Xamarin Studio 5.0 you can find the
*Restore Packages* under *Project* menu.

Before compiling any of the projects, there is one last file you need to edit.
[Phoebe/Build.cs](https://github.com/toggl/mobile/blob/master/Phoebe/Build.cs) contains various
configuration parameters for different components, which you need to fill in for the app to run.

## Contributing

Want to contribute? Great! Just [fork](https://github.com/toggl/mobile/fork) the project, make your
changes and submit a [pull request](https://github.com/toggl/mobile/pulls).

### Code style

There is a pre-commit git hook, that prevents commits with invalid code style. To reformat all of
the source files, just run:

	$ make format

## We are hiring!

Check out our [jobs page](http://jobs.toggl.com/) for current open positions.

## License

The code in this repository is licensed under the [BSD 3-clause license](https://github.com/toggl/mobile/blob/master/LICENSE).
