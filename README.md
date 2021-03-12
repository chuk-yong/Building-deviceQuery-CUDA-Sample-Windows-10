# Building-deviceQuery-CUDA-Sample-Windows-10

nVidia CUDA installation guide for Windows - 2.5 verifying the installation  
Requires you to build the deviceQuery.exe.  Here's the procedure using Visual Studio 2019

## Copy files to VS Studio project folder
Goto C:\ProgramData\NVIDIA Corporation\CUDA Samples\v8.0\1_Utilities\deviceQuery.  You may need to unhide \ProgramData if it is not visible.
Copy the folder to your VS Studio project folder.  For my case, it is:  
C:\Users\User\Documents\Visual Studio 2019\nVidia Project

## Launch Visual Studio 2019

<img src="LauchVS.PNG" width="450">

Then look for deviceQuery_vs2019.sln

<img src="Opensln.PNG" width="450">

Click to open deviceQuery.cpp file in Solution Explorer

<img src="Opencpp" width="450">

Notice < helper_cuda.h> is underlined in red.  The pciture doesn't show the actual red underline because I had already build the solution.

<img src="helper.PNG" width="450">

Right click the project name deviceQuery in Solution Explorer and go all the way down to the bottom and select Properties

<img src="properties.PNG" width="450">

This will appear

<img src="vcc.PNG" width="450">

In the left panel, select VC+ + Directories, then in the main panel, select Include Directories.  Click on the small down arrow and the end of the line.

<img src="include.PNG" width="450">

Add this line: C:\ProgramData\NVIDIA Corporation\CUDA Samples\v8.0\common\inc

<img src="addinc.PNG" width="450">

Apply and OK

Note that the red underline < helper_cuda.h> has disappeared

<img src="nored.PNG" width="450">

Select Build from the menu bar and Build Solution

<img src="build.PNG" width="450">

Five files: deviceQuery.exe, deviceQuery.lib, deviceQuery.exp, deviceQuery.ilk, and deviceQuery.pdb  will be generated in the directory C:\Users\User\Documents\Visual Studio 2019\bin\win64\Debug

Run the deviceQuery.exe to verify your CUDA installation













