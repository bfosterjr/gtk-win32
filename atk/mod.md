 * Download [ATK 2.5.91](http://ftp.acc.umu.se/pub/gnome/sources/atk/2.5/atk-2.5.91.tar.xz)
 * Extract to `C:\mozilla-build\hexchat`
 * In `build\win32\vs10\atk.props`, replace:
	* `intl.lib` with `libintl.lib`
	* `<AtkEtcInstallRoot>..\..\..\..\vs10\$(Platform)</AtkEtcInstallRoot>` with  
`<AtkEtcInstallRoot>..\..\..\..\build\$(Platform)</AtkEtcInstallRoot>`
	* `<CopyDir>$(AtkEtcInstallRoot)</CopyDir>` with  
`<CopyDir>..\..\..\..\atk-2.5.91-rel</CopyDir>`
	* `<AtkSeparateVS10DllSuffix>-1-vs10</AtkSeparateVS10DllSuffix>` with  
`<AtkSeparateVS10DllSuffix>-1.0</AtkSeparateVS10DllSuffix>`
 * Open `build\win32\vs10\atk.sln` with VS
 * Build in VS
 * Release with `release-x86.bat`
 * Extract package to `C:\mozilla-build\hexchat\build\Win32`
