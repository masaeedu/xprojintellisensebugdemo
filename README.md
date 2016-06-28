# xprojintellisensebugdemo
Demonstrates ReSharper bug in xproj + project.json projects with mixed TFMs. 

The referencer project targets net461, whereas the referencee project targets netstandard1.3. The latter is compatible with the former, as can be seen from successful msbuild and dotnet CLI compilation, and lack of Intellisense errors in vanilla Visual Studio 2015. 

However, when ReSharper is enabled, Intellisense errors can be seen in all API usage from the referenced library. The image below shows errors in the namespace import and instantiation of a class from the referenced library:

![ReSharper error in valid code](https://qjlqkg.by3302.livefilestore.com/y3m1GEvhJopBVRntFSMIXvCnIMWA_FAjtXHwx8m4V7GgFgOp_AQLrAb313-bVCAO_4woyBBQN_C8z7Af3Rgv47_Jf7NaUwF9dpvLEapZ9wIwH5U4MLwVQ9eTb8UVAUU9QtXDma17lH_ePsptSzjG8xUUsH8ylKDvxJyDk1IPdEj4ds/devenv_2016-06-28_19-00-19.png?psid=1)

ReSharper version: 2016.1.2
Visual Studio version: 14.0.25123.0
Windows 8 x64
