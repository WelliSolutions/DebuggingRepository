# Debugging Repository
A list of tools and information helpful for debugging.

## .NET

### Profiler

CLR Profiler, Microsoft [Github](https://github.com/microsoftarchive/clrprofiler/), [Wikipedia](https://en.wikipedia.org/wiki/CLR_Profiler) - status: archived, no longer maintained; MIT license

### Decompiler

dnSpy [Github](https://github.com/dnSpy/dnSpy) - status: archived, no longer maintained; GPLv3 license

dotPeek, Jetbrains [Download](https://www.jetbrains.com/decompiler/download/#section=portable) - free version available

ILSpy, Microsoft [Github](https://github.com/icsharpcode/ILSpy) - MIT license

JustDecompile, Telerik [Download](https://www.telerik.com/products/decompiler.aspx), [direct Download](https://www.telerik.com/try/justdecompile) - with an open source engine [Github](https://github.com/telerik/justdecompileengine) under Apache 2.0 license

Reflector, Redgate - [Download](https://www.red-gate.com/products/dotnet-development/reflector/) - commercial product ~100€ per user

### Deobfuscation, Unprotection

NETUnpack, Erik Pistelli [Download](https://ntcore.com/?page_id=353)

SNSRemover, Erik Pistelli [direct download](https://ntcore.com/files/SNSRemover.zip) - removes strong name signatures

### Debugger

MDbg, Microsoft [Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/framework/tools/mdbg-exe) - .NET command line debugger

SOS, Microsoft - extension for WinDbg in order to deal with managed applications. Comes with .NET Framework. Try `.loadby sos clr` for .NET 4, `.loadby sos coreclr` for .NET Core and Silverlight , `.loadby sos mscorwks` or `loadby sos mscorsvr` for .NET 2

SOSEx, Steve Johnson [Download](http://www.stevestechspot.com/)- extension for WinDbg, adding features that are missing in SOS

msos, Sasha Goldshtein [Github](https://github.com/goldshtn/msos) - .NET command line debugger; alternative for WinDbg + SOS; MIT license

### WPF

Snoop [Github](https://github.com/snoopwpf/snoopwpf) - WPF spy, Visual inspector, MS-PL license

### Other

Exctrlst, Microsoft [Article](https://techcommunity.microsoft.com/t5/ask-the-performance-team/two-minute-drill-disabled-performance-counters-and-exctrlst-exe/ba-p/374538) - Extensible Counter List tool; was part of the Windows 2000 Resource Kit; status: probably outdated

Hawkeye [Github](https://github.com/odalet/Hawkeye2) - edit .NET objects in memory; status: probably abandoned

Managed Stack Explorer (MSE) [Github](https://github.com/artisticcheese/MSE)

Sharplab [online tool](https://sharplab.io) - use `Inspect.Heap(new X());` to see the memory layout of an object

### People

0xd4d [Github](https://github.com/0xd4d)

Sasha Goldshtein [Twitter](https://twitter.com/goldshtn)

Steve Johnson [Website](http://www.stevestechspot.com/)



