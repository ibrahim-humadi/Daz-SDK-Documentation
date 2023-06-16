# Daz SDK Documentation
 A Cheatsheet for Users learning to use Daz3d's SDK <br>
<br>
 Getting started with the SDK:<br>
<br>
You will need to download:<br>
Cmake (>3.10)// https://cmake.org/download/<br>
Microsoft Visual Studio 2010 Professional // can be found online<br>
<br>
I installed/put my daz SDK folder here: "C:\Users\username\Documents\DAZ 3D\Studio\My Library\DAZStudio4.5+ SDK\"
navigate to this folder^<br>
Create a folder <b>build</b> here.<br>
Create a folder <b>64</b> inside <b>build</b>^<br>
<br>
Launch Cmake<br>
Click the <b>"Browse Source..."</b> button and navigate to the SDK root folder. eg: "C:\Users\username\Documents\DAZ 3D\Studio\My Library\DAZStudio4.5+ SDK\"<br>
Click the <b>"Browse Build..."</b> button and navigate to "build\64\" folder we created earlier. eg: "C:\Users\username\Documents\DAZ 3D\Studio\My Library\DAZStudio4.5+ SDK\build\64"<br>
Select <b>"Visual Studio 12 2013"</b> as the generator for the project.<br>
Select <b>"x64"</b> as the optional platform.<br>
Type <b>"v100"</b> into the Optional toolset to use.<br>
Press the Finish button. <br>
You should see a bunch of name/value pairs appear in your Cmake GUI.<br>
Type/Paste your Daz Studio directory containing DAZStudio.exe into the value for the name DAZ_STUDIO_EXE_DIR eg: "C:\Daz 3D\Applications\64-bit\DAZ 3D\DAZStudio4"<br>
Click <b>Generate</b> button in cmake GUI and wait for the build to complete.<br>
Close Cmake<br>
Navigate to "\DAZStudio4.5+ SDK\build\64\" and open "DAZ Studio SDK.sln" (In Visual Studio 2017)<br>
Build the solution<br>
If all went well you should now have a bunch of SDK sample plugins created at your daz exe's directory. In my case in: "C:\Daz 3D\Applications\64-bit\DAZ 3D\DAZStudio4\plugins\"<br>
You can check to see if they compiled correctly by opening Daz and clicking on the help menu and then clicking on "About installed plugins". Scroll through the plugins and see if the plugins with "(SDK Example)" in their names are loaded correctly<br>
<br>
<br>
Troubleshooting<br>
