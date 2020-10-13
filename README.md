## Info

This repository is meant do demo and reproduce an issue in Blazor Wasm with the HttpClient. Using a differnt syntax for registring this service in the `Program.cs` causes an error with the Release build.

`builder.Services.AddScoped<HttpClient>();` breaks while </br> `builder.Services.AddScoped(sp => new HttpClient());` works fine.

I was not able to reproduce this issue with the .NET 5 RC2 SDK.

SDK used is dotnet Core 3.1.402
Editor is Visual studio 2019 Community Version 16.7.5
