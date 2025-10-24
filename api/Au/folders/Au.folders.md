# Class `Au.folders`

Gets known/special folder paths (Desktop, Temp, etc).

```
public static class folders
```

##### Remarks

Most functions return `Au.Types.FolderPath`, not `string`. It is implicitly convertible to `string`. Its operator `+` appends a filename or relative path string, with `\` separator if need. Example:

```
string s = folders.Desktop + "file.txt"; //C:\Users\Name\Desktop\file.txt
```

If a function cannot get folder path, the return value contains `null` string. Then the `+` operator would throw `System.ArgumentException`.

Some folders are known only on newer Windows versions or only on some computers. Some functions have a suffix like `_Win8` which means that the folder is unavailable on older Windows. Some known folders, although supported and registered, may be still not created.

Some folders are virtual, for example Control Panel. They don't have a file system path, but can be identified by a data structure `ITEMIDLIST`. Functions of the nested class `Au.folders.shell` return it as `Au.Types.Pidl` or string `":: ITEMIDLIST"` that can be used with some functions of this library (`Au.run.it`, `Au.icon.of`, `Au.icon.ofPidl`) but not with .NET functions.

Most functions use Windows "Known Folders" API, such as `SHGetKnownFolderPath`. The list of Windows predefined known folders: `KNOWNFOLDERID`. Names of folders specific to current process have prefix `This`, like `ThisApp`.

Some paths depend on the bitness (32 or 64 bit) of the OS and this process.

|  |  |
| --- | --- |
| 32-bit Windows | `System`, `SystemX86`, `SystemX64`: `@"C:\WINDOWS\system32"`<br>`ProgramFiles`, `ProgramFilesX86`, `ProgramFilesX64`: `@"C:\Program Files"`<br>`ProgramFilesCommon`, `ProgramFilesCommonX86`, `ProgramFilesCommonX64`: `@"C:\Program Files\Common Files"` |
| 64-bit Windows, 64-bit process | `System`, `SystemX64`: `@"C:\WINDOWS\system32"`<br>`SystemX86`: `@"C:\WINDOWS\SysWOW64"`<br>`ProgramFiles`, `ProgramFilesX64`: `@"C:\Program Files"`<br>`ProgramFilesX86`: `@"C:\Program Files (x86)"`<br>`ProgramFilesCommon`, `ProgramFilesCommonX64`: `@"C:\Program Files\Common Files"`<br>`ProgramFilesCommonX86`: `@"C:\Program Files (x86)\Common Files"` |
| 64-bit Windows, 32-bit process | `System`: `@"C:\WINDOWS\system32"`. However the OS in most cases redirects this path to `@"C:\WINDOWS\SysWOW64"`. <br>`SystemX86`: `@"C:\WINDOWS\SysWOW64"`<br>`SystemX64`: `@"C:\WINDOWS\Sysnative"`. The OS redirects it to the true `@"C:\WINDOWS\system32"`. It is a special path, not in Explorer. <br>`ProgramFiles`, `ProgramFilesX86`: `@"C:\Program Files (x86)"`<br>`ProgramFilesX64`: `@"C:\Program Files"`<br>`ProgramFilesCommon`, `ProgramFilesCommonX86`: `@"C:\Program Files (x86)\Common Files"`<br>`ProgramFilesCommonX64`: `@"C:\Program Files\Common Files"` |

##### Inheritance

`object` → `folders`

### Properties

`AccountPictures_Win8`, `AdminTools`, `ApplicationShortcuts_Win8`, `CDBurning`, `CameraRoll_Win81`, `CdDvdDrive`, `CommonAdminTools`, `CommonOEMLinks`, `CommonPrograms`, `CommonStartMenu`, `CommonStartup`, `CommonTemplates`, `Contacts`, `Cookies`, `Desktop`, `DeviceMetadataStore`, `Documents`, `DocumentsLibrary`, `Downloads`, `Editor`, `Favorites`, `Fonts`, `GameTasks`, `History`, `ImplicitAppShortcuts`, `InternetCache`, `Libraries`, `Links`, `LocalAppData`, `LocalAppDataLow`, `LocalizedResourcesDir`, `Music`, `MusicLibrary`, `NetHood`, `NetRuntime`, `NetRuntimeBS`, `NetRuntimeDesktop`, `NetRuntimeDesktopBS`, `OriginalImages`, `PhotoAlbums`, `Pictures`, `PicturesLibrary`, `Playlists`, `PrintHood`, `Profile`, `ProgramData`, `ProgramFiles`, `ProgramFilesCommon`, `ProgramFilesCommonX64`, `ProgramFilesCommonX86`, `ProgramFilesX64`, `ProgramFilesX86`, `Programs`, `Public`, `PublicDesktop`, `PublicDocuments`, `PublicDownloads`, `PublicGameTasks`, `PublicLibraries`, `PublicMusic`, `PublicPictures`, `PublicRingtones`, `PublicUserTiles_Win8`, `PublicVideos`, `QuickLaunch`, `Recent`, `RecordedTV`, `RemovableDrive0`, `RemovableDrive1`, `RemovableDrive2`, `RemovableDrive3`, `ResourceDir`, `Ringtones`, `RoamedTileImages_Win8`, `RoamingAppData`, `RoamingTiles_Win8`, `SampleMusic`, `SamplePictures`, `SamplePlaylists`, `SampleVideos`, `SavedGames`, `SavedPictures`, `SavedPicturesLibrary`, `SavedSearches`, `Screenshots_Win8`, `SearchHistory_Win81`, `SearchTemplates_Win81`, `SendTo`, `SidebarDefaultParts`, `SidebarParts`, `SkyDriveCameraRoll_Win81`, `SkyDriveDocuments_Win81`, `SkyDrivePictures_Win81`, `SkyDrive_Win81`, `StartMenu`, `Startup`, `System`, `SystemX64`, `SystemX86`, `Temp`, `Templates`, `ThisApp`, `ThisAppBS`, `ThisAppDataCommon`, `ThisAppDataLocal`, `ThisAppDataRoaming`, `ThisAppDocuments`, `ThisAppDriveBS`, `ThisAppImages`, `ThisAppTemp`, `TreeProperties`, `UserProfiles`, `UserProgramFiles`, `UserProgramFilesCommon`, `Videos`, `VideosLibrary`, `Windows`, `Workspace`, `WorkspaceDriveBS`, `noAutoCreate`

### Methods

`envVar`, `getFolder`, `getKnownFolders`, `removableDrive`, `removableDrive`, `sourceCode`, `sourceCodeMain`, `unexpandPath`, `unexpandPath`, `unexpandPath`