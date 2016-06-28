# xprojintellisensebugdemo
Demonstrates Resharper bug in xproj + project.json projects with mixed TFMs. 

The referencer project targets net461, whereas the referencee project targets netstandard1.3. The latter is compatible with the former, as can be seen from successful msbuild and dotnet CLI compilation, and lack of Intellisense errors in vanilla Visual Studio 2015.

Resharper version: 2016.1.2
Visual Studio version: 14.0.25123.0
Windows 8 x64
