https://www.w3.org/WAI/WCAG21/quickref/
https://ourcodeworld.com/articles/read/353/how-to-convert-numbers-to-words-number-spelling-in-javascript


https://ieeexplore.ieee.org/abstract/document/9685695
https://github.com/nodejs/node-gyp/blob/main/docs/Updating-npm-bundled-node-gyp.md



18

After spending a while to get this to work (for me accepted answer didn't work, for me it's just half solution) i did following:

Sadly, you must have visual studio (i installed express edition 2013 for DESKTOP)

Installed python 2.7.3 (you don't have to set any environment variables)

Run cmd as administrator and go to you project root (where is you package.json file)

First run: npm config set python C:\Python27\python.exe

Then: npm install -msvs_version=2013

The trick is in command npm config set python ...path_to_python_exe... which will be provided by npm to dependency which needs python i guess. I don't know why setting python as env variable is not enough.



++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Delete C:\Users\user_name\.node-gyp

Delete %AppData%/npm

Delete %AppData%/npm-cache

And install node-gyp again

Following instruction on node-gyp page

I chose Option 1 npm install --global --production windows-build-tools

+++++++++++++++https://stackoverflow.com/questions/21562038/node-gyp-build-error-windows-x64++++++++++++++++++++
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

https://github.com/nodejs/node-gyp/issues/1663
===================================================================================================================
**************************************************************************************************************************************************************************************************************************************https://github.com/nodejs/node-gyp/issues/1663#issuecomment-502213785*****************************************************************************************************************************************************************************************************************************
npm config set msbuild_path "C:\Program Files (x86)\Microsoft Visual Studio\2019\Enterprise\MSBuild\Current\Bin\MSBuild.exe"
