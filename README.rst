============
Branch Build
============

Build for make clean build to specific git branch. For example: I'm
using it to build sphinx documentation to gh-pages branch.
     
If build branch is exists locally - it will be resetted to remote 
origin before build. If remote origin doesn't exist - it will be 
recreated locally. Anyway - branch will be cleaned before build.
This behaviour prevents any corruption and lots of commits.
     
After build all changes will be pushed to target branch in work 
local repository. If your local work repository is clone of 
remote - you need to push changes.

Requirements
============

  - Ant
  - Git. In Windows you must install it with "command promt" option.

Usage
=====

Edit branch-build.properties file. All variables are commented.

Building process runs to directory specified by ${build.dir} 
variable branch-build.properties file. Sub-Ant buildfile specified by 
${build.builder} variable in build-to-branch.properties file called 
with ${build.dir} variable.

Edit ${build.builder} sub-Ant buildfile. Regardless of location of 
sub-Ant buildfile ${basedir} variable will be same as in the parent 
branch-build.xml.

Enjoy. Let's make life better.