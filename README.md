.sbt
====

My SBT global settings.  Clone this directory into your home directory.  Also contains notes on setting up Scala dev environment.

Sublime Text 2 Development
==========================

* ensime-sbt-plugin - Generates .ensime project files.  ENSIME gives you compiler error checking, autocomplete,
      type hints, and more.
* sbt-sublime - Allows you to browse third party dependencies!!

1. First, in your project dir, do "rm -rf project/target".  This is important for generating accurate .ensime
   project files, otherwise the autocomplete and other features may not work.
2. From sbt shell, "ensime generate".  Should be fairly fast.
3. From sbt shell, "gen-sublime".  This takes a long time, tries to download every source JAR, and creates a
   sublime project file.
4. Open the project file: "subl my-project.sublime-project"

Now you should have all the goodies: Ctrl-space autocomplete, error checking on save, Cmd-P go to source for
third party dependencies.