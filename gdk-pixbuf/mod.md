 * Download [GDK-PixBuf 2.26.4](http://ftp.gnome.org/pub/gnome/sources/gdk-pixbuf/2.26/gdk-pixbuf-2.26.4.tar.xz)
 * Extract to `C:\mozilla-build\hexchat`
 * In `build\win32\vs10\gdk-pixbuf.props`, replace:
	* `intl.lib` with `libintl.lib`
	* `<GlibEtcInstallRoot>..\..\..\..\vs10\$(Platform)</GlibEtcInstallRoot>` with  
`<GlibEtcInstallRoot>..\..\..\..\build\$(Platform)</GlibEtcInstallRoot>`
	* `<CopyDir>$(GlibEtcInstallRoot)</CopyDir>` with  
`<CopyDir>..\..\..\..\gdk-pixbuf-2.26.4-rel</CopyDir>`
	* `<GdkPixbufSeparateVS10DllSuffix>-2-vs10</GdkPixbufSeparateVS10DllSuffix>` with  
`<GdkPixbufSeparateVS10DllSuffix>-2.0</GdkPixbufSeparateVS10DllSuffix>`
 * Replace `zlib1.lib` with `zdll.lib` in `build\win32\vs10\gdk-pixbuf.vcxproj`
 * Open `build\win32\vs10\gdk-pixbuf.sln` with VS
 * Build in VS
 * Release with `release-x86.bat`
 * Extract package to `C:\mozilla-build\hexchat\build\Win32`
