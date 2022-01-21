# Debugging Repository
A list of tools and information helpful for debugging.

## Monitoring, Recording, Profiling

API Monitor, Rohitab [Download](http://www.rohitab.com/apimonitor)

Process Monitor, Mark Russinovich / Microsoft [Download](https://docs.microsoft.com/en-us/sysinternals/downloads/procmon)

## Inspection

CFF Explorer Suite [Download](https://ntcore.com/?page_id=388) - Inspection for Portable Executables (PE)

ChkMatch [Download from archive.org](https://web.archive.org/web/20210205095232/https://www.debuginfo.com/tools/chkmatch.html) - Checks whether PDB and DLL/EXE match

DebugDir [Download](https://sourceforge.net/p/debugdir/home/Home/) - originally developed by Oleg Starodumov

DebugView++ [Github](https://github.com/CobaltFusion/DebugViewPP) - a faster alternative to DebugView; BSL license

DebugView, Mark Russinovich / Microsoft [Download](https://docs.microsoft.com/en-us/sysinternals/downloads/debugview) - this is the original, but use DebugView++ instead, because they improved it really well

Dependencies [Github](https://github.com/lucasg/Dependencies) - more recent version of Dependency Walker

Dependency Walker [Download](https://www.dependencywalker.com/) - seems to have problems with recursive DLL imports; status: probably abandoned

Process Explorer, Microsoft [Download](https://docs.microsoft.com/en-us/sysinternals/downloads/process-explorer?redirectedfrom=MSDN) 

DynLogger, NTCore [Download](https://ntcore.com/?page_id=376)

## System diagnosis

Driver List, NTCore [Download](https://ntcore.com/?page_id=380)

Filter Monitor, NTCore [Download](https://ntcore.com/?page_id=382)

## Logging

MS Build Log Viewer [Download](https://msbuildlog.com/)

## Native

### Creating Crash Dumps

Visual Studio, Microsoft [Download](https://visualstudio.microsoft.com/downloads/) - Community edition is free

ProcDump, Mark Russinovich / Microsoft [Download](https://docs.microsoft.com/en-us/sysinternals/downloads/procdump) - will detect bitness automatically (or specify `-64`)

WinDbg, Microsoft [Download](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugger-download-tools) - `.dump /ma <filename>.dmp` will use the bitness of the debugger you used for attaching

Process Explorer, Microsoft [Download](https://docs.microsoft.com/en-us/sysinternals/downloads/process-explorer?redirectedfrom=MSDN) - will detect bitness automatically

Windows Error Reporting LocalDumps Registry key, Microsoft [Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/wer/collecting-user-mode-dumps?redirectedfrom=MSDN)

DebugDiag, Microsoft [Download](https://www.microsoft.com/en-us/download/details.aspx?id=58210) - will create dumps with the same bitness as DebugDiag

ADPlus, Microsoft - part of WinDbg, will create dumps with the same bitness as ADPlus

### Memory Leaks

LeakDiag - status: super old, only works on Windows XP

Visual Leak Detector [Download](https://kinddragon.github.io/vld/) - GPL v2.1 license; status: probably abandoned

UMDH, Microsoft [Microsoft Docs](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/umdh) - part of WinDbg

UMDH GUI, ATrefzer [Github](https://github.com/ATrefzer/UmdhGui) - MIT license; graphical user interface for UMDH

### Other

Application Verifier, Microsoft [Microsoft Docs](https://docs.microsoft.com/en-us/windows-hardware/drivers/devtest/application-verifier) - is part of the Windows SDK

EZ Application Verifier [Github](https://github.com/WelliSolutions/EZ-Application-Verifier) - enable Application Verifier and LocalDumps for a lot of executables

GFlags, Microsoft - is part of WinDbg

DebugDiag, Microsoft [Download](https://www.microsoft.com/en-us/download/details.aspx?id=58210)

### WinDbg

WinDbg, Microsoft [Download](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugger-download-tools) - is part of the Windows SDK

WinDbg Preview, Microsoft [Windows Store](https://www.microsoft.com/store/p/windbg/9pgjgd53tn86) - has a much nicer usability and seems as stable as the regular version

#### Cheat Sheets & Command Trees

WinDbg Cheat Sheet, ATrefzer [Github](https://github.com/ATrefzer/WinDbg)

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

### .NET Core

dotnet-dump, Microsoft [Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/core/diagnostics/dotnet-dump) - collect and analyze .NET Core crash dumps, similar to ProcDump or DebugDiag

dotnet-counters, Microsoft [Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/core/diagnostics/dotnet-counters) - performance counters for .NET Core

dotnet-gcdump, Microsoft [Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/core/diagnostics/dotnet-gcdump) - memory snapshots for leak analysis

dotnet-trace, Microsoft [Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/core/diagnostics/dotnet-trace) - performance analysis utility

dotnet-symbol, Microsoft [Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/core/diagnostics/dotnet-symbol) - downloads .NET COre symbols

dotnet-sos, Microsoft [Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/core/diagnostics/dotnet-sos) - SOS for .NET Core

### Other

Exctrlst, Microsoft [Article](https://techcommunity.microsoft.com/t5/ask-the-performance-team/two-minute-drill-disabled-performance-counters-and-exctrlst-exe/ba-p/374538) - Extensible Counter List tool; was part of the Windows 2000 Resource Kit; status: probably outdated

Hawkeye [Github](https://github.com/odalet/Hawkeye2) - edit .NET objects in memory; status: probably abandoned

Managed Stack Explorer (MSE) [Github](https://github.com/artisticcheese/MSE)

Sharplab [online tool](https://sharplab.io) - use `Inspect.Heap(new X());` to see the memory layout of an object

## People

0xd4d [Github](https://github.com/0xd4d)

Sasha Goldshtein [Twitter](https://twitter.com/goldshtn)

Steve Johnson [Website](http://www.stevestechspot.com/)

Mark Russinovich [Wikipedia](https://en.wikipedia.org/wiki/Mark_Russinovich), [Website](http://markrussinovich.com/), [Twitter](https://twitter.com/markrussinovich) - author or Windows Internals books, now CTO of Microsoft Azure

Oleg Starodumov, author of debuginfo.com (down) and Microsoft MVP [Blogspot](http://starol.blogspot.com/), [Microsoft MVP Blogs](https://blogs.msmvps.com/debuginfo/)

Tess Ferrandez [Blog](https://www.tessferrandez.com/) - former Microsoft Escalation Engineer, debugging ASP .NET with WinDbg
