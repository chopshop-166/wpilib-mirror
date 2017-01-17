WPILib Mirror
=============

Deprecated
----------

This repository used to contain a mirror of the code releases for [WPILib][].
Because the code is now located on [GitHub][], as well as available
[via Maven][Maven], this repository is being replaced with instructions on
setting up a repository to pull the dependencies from [Maven][].

For backward-compatibility's sake, the old files are still accessible via tag,
but their usage is discouraged.
For any continued support, the appropriate version of WPILib should be used.
The Maven releases only support 2016 (named `wpilibJavaFinal`) and 2017 (named
`athena`) versions of the library.

As of 2017, this repository will not receive any WPILib updates directly,
but *might* update the latest version number.

About
-----

This repository contains two files.
The `.travis.yml` tells [Travis-CI][] to use its java setup for testing.
By [default][Travis-CI defaults], Travis will attempt to build using Maven,
Gradle, or Ant.
For convenience, [Chop Shop 166][] uses Maven.
The `pom.xml` file contains Maven boilerplate and dependency management.

**Note**: Using these files ignores any changes done in either
`build.properties` or `build.xml`.

Setup
-----

The simplest setup is to copy `.travis.yml` and `pom.xml` into the team's git
repository. After that, the following tags within `pom.xml` need to be changed:

- `groupId`: The Java base package - for example, `org.usfirst.frc.team166`.
  This must match the structure of the `src/` repository (probably generated by
  Eclipse)
- `name`: The repository name *optional*
- `url`: The URL the repository is canonically located at *optional*
- `version`: For each dependency, the version should be kept in sync with the
  most recent library version

[WPILib]: http://wp.wpi.edu/wpilib
[GitHub]: https://github.com/wpilibsuite/allwpilib
[Maven]: http://first.wpi.edu/FRC/roborio/maven/release
[Travis-CI]: http://travis-ci.org
[Travis-CI defaults]: https://docs.travis-ci.com/user/languages/java/
[Chop Shop 166]: http://chopshop166.com
