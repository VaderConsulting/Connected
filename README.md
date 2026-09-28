# Connected

VB.NET WinForms tool that enumerates SMB sessions and open files on a chosen computer. `frmMain` calls `clsConnection.GetConnections` / `GetOpenFiles` (Netapi32 `NetFileEnum` and related session APIs) and builds a tree of computers, users, idle time, connect time, and open paths. Radio buttons switch computer-centric versus user-centric views. Administrators use it to see who is connected to a file server and which files they hold open.

**Source last updated:** 2004-08-17  
**Language:** VB.NET  
**Target:** .NET Framework (Visual Studio .NET 2003 solution format)  
**Output:** WinForms executable (`ConnectedUsers` project name in the solution)

## Solution structure

| Project | Language | Type | Purpose |
| --- | --- | --- | --- |
| `ConnectedUsers` | VB.NET | WinForms exe | Enumerate sessions and open files; tree UI on `frmMain` |

## How to open

Open `ConnectedUsers.sln` in Visual Studio .NET 2003 or later that still opens Format Version 8.00 solutions. `clsConnection.vb` and the `.vbproj` may appear as `.example` redacted copies in this tree.

## Requirements

- Visual Studio .NET 2003 or Visual Studio 2005 to 2010 (for Format Version 8.00)
- .NET Framework matching the project file
- Network rights to call Netapi32 session/file enum APIs on the target computer

## Attribution and provenance

Working copy from my Historical Dev folder. This folder is a near-duplicate of the `ConnectedUsers` repository (same solution and form sources).

## License

MIT. See `LICENSE`.
