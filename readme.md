# My Symbols Server

使用[SymbolSource.Server.Basic](http://www.symbolsource.org/Public/Blog/View/2012-03-13/Releasing_the_community_edition_of_SymbolSource)搭建私有的调试服务器。

## 关键步骤:

- 1 部署MySymbols到IIS，确保首页正常访问。
- 2 点击首页的诊断链接（Run self-diagnostics），查看自检状态。
- 3 根据自检状态，修正错误
- 4 安装wdk调试工具(演示主机环境是2012R2，可使用wdk8.1_auto_download.exe)，下载并安装。
- 5 VS中，工具，设置，调试，常规，反勾选“启用仅我的代码”，选中启用源服务器支持。
- 6 VS中，工具，设置，调试，符号，设置Symbols服务器地址（按首页提示的地址，例如http://{YOURSITEURL}/MySymbols/WinDbg/pdb），设置一个没有特殊权限的缓存目录，例如C:\SymbolCache

## 一些注意事项：

- 如果自检中发现SrcSrvPath配置有错误（SrcSrvPath Configuration Test - Directory not found），检查web.config中的SrcSrvPath根据实际操作系统的不同，路径可能不同，注意安装的正确位置!
- 如果自检中发现push有错误（NuGet Push Test - InternalServerError），可以尝试将应用池启用32位设置，然后再试。

## some useful links

- [nuget.org](https://www.nuget.org/)
- [Creating symbol packages](https://docs.microsoft.com/en-us/nuget/create-packages/symbol-packages#referring-to-files-in-the-nuspec)
- [Releasing the community edition of SymbolSource](http://www.symbolsource.org/Public/Blog/View/2012-03-13/Releasing_the_community_edition_of_SymbolSource)
- [Is it possible to host both regular and symbols packages in a NuGet local feed on a network share?](https://stackoverflow.com/questions/45620764/is-it-possible-to-host-both-regular-and-symbols-packages-in-a-nuget-local-feed-o)
- [Serve up Debug Symbols for your NuGet packages? Heck yeah!](http://netitude.bc3tech.net/2015/01/12/serve-up-debug-symbols-for-your-nuget-packages-heck-yeah/)
