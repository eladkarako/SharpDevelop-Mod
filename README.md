no releases,  
just download it all with:  
https://github.com/eladkarako/SharpDevelop-Mod/archive/refs/heads/master.zip  

<hr/>

# SharpDevelop-Mod

v5.1.0.52.16 original code. <br/>
made portable <br/>
and manifest-patched for crispy clear display in Windows 10. <br/>
+StyleCop +FxCop if you need it. <br/>
<h1>no support!</h1>

<hr/>

support should go to the original creator.  
start.cmd is all you need.  
you can modifiy it to your likeing.  

<hr/>

the following manifest from https://github.com/eladkarako/manifest/  
was applied (when needed) to various dlls and exe files:  

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
  <dependency> 
    <dependentAssembly> 
      <assemblyIdentity name="Microsoft.Windows.Common-Controls" 
        version="6.0.0.0" publicKeyToken="6595b64144ccf1df" 
        type="win32" processorArchitecture="*" language="*" /> 
    </dependentAssembly> 
  </dependency> 
  <application xmlns="urn:schemas-microsoft-com:asm.v3"> 
     <windowsSettings> <dpiAware      xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">true/PM</dpiAware>                     </windowsSettings> 
     <windowsSettings> <dpiAwareness  xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">PerMonitorV2,PerMonitor</dpiAwareness> </windowsSettings> 
     <windowsSettings> <longPathAware xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">true</longPathAware>                   </windowsSettings> 
     <windowsSettings> <heapType      xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">SegmentHeap</heapType>                 </windowsSettings> 
  </application> 
  <trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
      <requestedPrivileges> 
        <requestedExecutionLevel level="asInvoker" uiAccess="false" /> 
      </requestedPrivileges> 
    </security> 
  </trustInfo> 
  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
      <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}" /> 
      <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}" /> 
      <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}" /> 
      <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}" /> 
      <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}" /> 
    </application> 
  </compatibility> 
</assembly> 
 
```

controls might seems a bit glitchy,  
feel free to repatch every dll and exe with the additional <code>gdiScaling</code> (see manifest project link),  
which might fix it.

```xml
<windowsSettings> <gdiScaling xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">true</gdiScaling>                         </windowsSettings>  <!-- makes graphic programs such as ones that takes screenshots have bad functionality with larger-DPI (ease of access), since it also enlarges the controls in sub containers, and somtimes breaks the UI, for non-graphic-programs it might improve scale text and standard controls in apps, prevents blur. useful if you are using non 100% DPI for example in 'ease-of-access'. https://docs.microsoft.com/en-us/windows/win32/sbscs/application-manifests#gdiscaling -->
```

<hr/>

no support.