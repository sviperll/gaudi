Gaudi
=====

Easy to use build system with minimum, almost zero config.

Features
--------

Fast: it's really fast, since it's single bash script :P
Capable: it's possible to download artifacts from maven central which is great for single bash script.

Project structure
-----------------

 * `build` - automatically generated directory where all generated files are put
 * `src` - directory for Java sources
 * `resources` - resources that should be present during run-time
 * `compile-resources` - resources that should be present only during compilation, i. e. templates for generated code
 * `compile-and-run-resources` - resources that should be present during both during compile-time and run-time

Commands
--------
 * `gaudi init PROJECT_NAME` - creates new directory for new PROJECT and creates some directories
 * `gaudi compile` - compiles project
 * `gaudi run` - runs project
 * `gaudi compile-classpath` - prints out compile time classpath
 * `gaudi run-classpath` - prints out run time classpath
 * `gaudi artifact-file ARTIFACT VERSION` - downloads artifact from maven central if nessesary and
   prints file name corresponding to given `ARTIFACT` and `VERSION`
 * `gaudi artifact-versions ARTIFACT` prints available versions for given `ARTIFACT`
 * `gaudi new class CLASS_NAME` creates new java file for given class in current directory/package
 * `gaudi new interface INTERFACE_NAME` creates new java file for given interface in current directory/package
 * `gaudi new enum INTERFACE_NAME` creates new java file for given enum in current directory/package

You can run gaudi commands in any subdirectories of project directory.
Project root is detected by `build-info.sh` file.
`gaudi new ...` commands only works from within sources directory.

Configuration
-------------

Configuration file "$XDG_CONFIG_HOME/gaudi.config" ("$HOME/.config/gaudi.config").
You can specify following variables in config file to customize gaudi

 * `MAVEN_REPOSITORY` URL of maven repository (default is `https://repo1.maven.org/maven2`)

