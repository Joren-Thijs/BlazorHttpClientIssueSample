### Info

This repository is meant do demo and reproduce an issue in Blazor WASM with the HttpClient. Using a differnt syntax for registring this service in the `Program.cs` causes an error with the Release build.

### To Reproduce

Minimal repo with reproduction: https://github.com/Joren-Thijs/BlazorHttpClientIssueSample

To reproduce this issue replace in `Program.cs`
`builder.Services.AddScoped(sp => new HttpClient());` with
`builder.Services.AddScoped<HttpClient>();`

And then access the "fetch data" page in the app.

### Technical details

-   SDK used is dotnet Core 3.1.402
-   The IDE used is Visual studio 2019 Community Version 16.7.5

### Exceptions

I was not able to reproduce this issue with the .NET 5 RC2 SDK.
