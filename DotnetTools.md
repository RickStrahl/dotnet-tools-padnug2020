# Using .NETCore Tools to Create Reusable and Shareable Tools & Apps

Starting with .NET Core 2.1 Microsoft introduced the **Dotnet Tools** platform as part of the .NET Core SDK. 

Dotnet Tools are a simple way to create, publish and consume what are essentially .NET Core Console applications that can be published and shared using the existing NuGet infrastructure for packaging and distribution. This means it's really easy to build tools that you can share with others either publicly or privately. 

The idea is to make easy to build, publish and consume executable tools in the same way you've been able create NuGet packages for .NET Core components in the past.

And while the original idea was to build tools to aid as part of the build process, this platform really offers much more scope because essentially you can publish and share any .NET Core Console application on it. This includes building servers that run full ASP.NET Core applications or full services. 

The big selling point of Dotnet Tools is this:

* You can **build** a tool with a simple flag in your .NET Project file
* You can **publish** the tool to NuGet like any other NuGet Package
* You can **install** a tool via `dotnet tool install`
* You can **update** and **uninstall** Dotnet Tools

The only pre-requisite to consuming a Dotnet Tool installed with `dotnet tool install` is the .NET Core SDK which is required to run tools. Tool packages are very small because they contain only the compiled .NET Core binaries - the runtimes are provided by the required .NET Core SDK dependency.

Specifically the fact that you can **easily** publish tools using the existing NuGet tooling infrastructure, that doesn't require extensive store like validation makes Dotnet Tools attractive because it lets you quickly create and interate, deploy new versions of tools.

If all this looks familiar from NodeJs and NPM - you're right. The idea is not new by any means, but certainly for .NET the idea of being able to easily publish and share binary executable tools is something new.

### What is a Dotnet Tool?
When you break what a Dotnet Tool is it comes down to this simple statement:

> “A Dotnet Tool is really like a glorified.NET Core Console Application that can be easily shared and installed via NuGet.”
>
> Me, 2020


