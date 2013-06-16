Sure, there are many ways to get started coding on msysGit.
While participating a 24h-hackathon, we've discovered a smart way
to code on msysGit under Windows, by using Eclipse.

#### Goals
* using an IDE - not only a text editor
* code syntax highlighting (sophisticated and able to recognize scopes)
* code navigation (clicking with mouse of using keyboard shortcuts)
* re-factoring (at least rename local variables, etc.)
* full and robust debugging support using actual C source code files
* preferred: smart search, not only RegEx ;-)
* nice to have: able to create build within the IDE

As it turns out, with a little knowledge about Eclipse, we've found everything solved by using Eclipse and a separate MinGW installation. The setup is pretty fast and can be done in less than one hour. If you know other Languages and IDEs, you may miss some features, but this setup solved our needs. 

#### Install required tools
1. Of course, first you need to setup msysGit
   * I've used the net installer
   * See [[InstallMSysGit]]
1. Download Eclipse C/C++ (current version Juno, 4.2 SR2)
   * unzip it somewhere (c:\program files\eclipse)
   * install Java JRE (current version 1.7) - a JRE is sufficient, but installing a JDK is highly recommended
1. Download MinGW
   * I've used net installer mingw-get-inst-20120426.exe 
   * install it
   * This is optional, but I recommend it because of newer gdb (debugger) version

#### Setup Eclipse Workspace
* Run eclipse and use a separate workspace folder, which is _NOT_ the msysgit installation folder
* create a new project
   * use the wizard to create a new C Proejct (simple C Project only)
   * name the project 'msysGit'
   * use all the wizard default settings and finish this step
* within the project create a linked folder to msysGit
   * folder-name: ```src-git```
   * click ```advanced```
   * click ```linked folder```
   * specify the msysGit installation path and the ```git``` folder within
   * [[create_linked_folder_to_msysgit.png]]