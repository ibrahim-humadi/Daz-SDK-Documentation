# Daz SDK Documentation
 A Cheatsheet for Users learning to use Daz3d's SDK <br>
<br>
 Getting started with the SDK:<br>
<br>
You will need to download:<br>
Cmake (>3.10)// https://cmake.org/download/<br>
Microsoft Visual Studio 2010 Professional // Hard ****** to find online but we need compiler<br>
I also used Visual Studio 2017 for actually building the plugins // Easy to find online<br>
<br>
I installed/put my daz SDK folder here: "C:\Users\username\Documents\DAZ 3D\Studio\My Library\DAZStudio4.5+ SDK\"<br>
navigate to this folder^<br>
Create a folder <b>build</b> here.<br>
Create a folder <b>64</b> inside <b>build</b>^<br>
<br>
Launch Cmake<br>
Click the <b>"Browse Source..."</b> button and navigate to the SDK root folder. eg: "C:\Users\username\Documents\DAZ 3D\Studio\My Library\DAZStudio4.5+ SDK\"<br>
<br>
Click the <b>"Browse Build..."</b> button and navigate to "build\64\" folder we created earlier. eg: "C:\Users\username\Documents\DAZ 3D\Studio\My Library\DAZStudio4.5+ SDK\build\64"<br>
<br>
<br>
Click the "Configure" button<br>
Select <b>"Visual Studio 12 2013"</b> as the generator for the project.<br>
<br>
Select <b>"x64"</b> as the optional platform.<br>
<br>
Type <b>"v100"</b> into the Optional toolset to use.<br>
<br>
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

If Cmake complains about MSbuild.exe missing during the configure/generation step then you need to add the folder containing your .net framework witht hat tool inside to your Path env variable.<br>
In my case thats at: "C:\Windows\Microsoft.NET\Framework64\v4.0.30319"<br>
So click your start button and type in "environment" and open "Edit the System environment variables" that is suggested to you (On windows 10)<br>
Click the "Environment Variables..." button.<br>
Select the User Variable "Path" and click edit.<br>
Click "New" and paste your directory here eg: "C:\Windows\Microsoft.NET\Framework64\v4.0.30319"<br>
Click "OK" on those windows we just opened and you should be good to go!<br>
<br>
<br>
If your Visual Studio complains about missing ammintrin.h then download it from: www.mathworks.com/matlabcentral/answers/uploaded_files/735/ammintrin.m<br>
rename this file^ to ammintrin.h and move it to "C:\Program Files (x86)\Microsoft Visual Studio 10.0\VC\include"<br>
