

# Test MonoGame-wasm on the Web

Demo hosted at Vercel  
[MonoGame-wasm - Demo](https://sdl-wasm-sample-web.vercel.app/docs/MonoGame/)

Tried also github pages but deployment took too long.  
Lost patience after 5 minutes. So I searched for an alternative.  
Found this: [Top 5 free website hosting platforms for your next project](https://dev.to/vishnusatheesh/5-static-website-hosting-platforms-for-your-next-project-2ahf)
and tried Vercel.

Sign-In and deployment in 2 min.




## Setup MonoGame-wasm

- Clone the two repositories below in the same folder  
  https://github.com/RedMike/MonoGame/tree/feature/dotnet-wasm  
  https://github.com/RedMike/SdlWasmSample/tree/monogame-net8  
  Ensure using the exact branches: `monogame-net8` and `dotnet-wasm`

- Add the ProjectReference to `SdlWasmSample.csproj`
    ```xml
    <ItemGroup>
        <ProjectReference Include="..\..\MonoGame\MonoGame.Framework\MonoGame.Framework.DesktopGL.csproj" />
    </ItemGroup>
    ```


## Deploy as static web page

Below the list of files added to repository for static web site hosting.
```
    index.html      (copied via devtools)
    main.js         (copied via devtools)
    _framework/
        blazor.boot.json
        dotnet.js
        dotnet.native.8.0.2.sxojud5nuz.js
        dotnet.runtime.8.0.2.8j60y5zbay.js
        *.wasm
        *.dat
```

The *.wasm and *.dat files are cached by the browser. So subsequent loads are fast.

The resulting folder structure - see [MonoGame](https://github.com/friflo/SdlWasmSample-web/tree/main/docs/MonoGame)



