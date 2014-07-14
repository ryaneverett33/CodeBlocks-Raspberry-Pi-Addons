CodeBlocks Addons [R-Pi]
==============================
Easy Cross Compilation for the Raspberry Pi from the Code::Blocks IDE. Tested and working on Ubuntu 14.04.

## Prerequisites
You must have the GCC Compiler installed on your linux device prior to installing this. Code::Blocks will be unable to locate the compiler if you don't. Information about installing the compiler can be found here: [Elinux.org](http://elinux.org/RPi_Kernel_Compilation). If you're on Ubuntu, this can be accomplished by running in terminal:
''''term
apt-get install gcc-arm-linux-gnueabi make ncurses-dev
''''
Then simply follow the instructions for installation.

## Installation
<b>Close down Code::Blocks before starting.</b>
Open Files with root priviledges.
'''term
gksu nautilus
'''
Navigate to /usr/share/codeblocks
Open the "compilers" folder and copy "compiler_rpi.xml" and "options_rpi.xml" into it.
Close the "compilers" folder, open up the "templates" folder, and then open the "wizards" folder. Copy the "raspberrypi" folder into this folder.
Open Code::Blocks and click FIle > Create a new Project.
Right-click in the white space and click "Edit global registration script".
Add the following lines to the script in the "RegisterWizards" function.
'''term
RegisterWizard(wizProject,     _T("raspberrypi"),  _T("Raspberry Pi application"),_T("Raspberry Pi"));
'''
Save, Close, and then Restart Code::Blocks for the project option to show up.

## Notes
The Compiler only compiles C scripts, any scripts compiled in C++ will not execute. Writing in C++ is forbidden. [FIX-ME] Upon creating a project, Code::Blocks will warn about three wizard errors, continue as normal. Projects still compile.
