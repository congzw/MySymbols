# My Symbols Server

ʹ��[SymbolSource.Server.Basic](http://www.symbolsource.org/Public/Blog/View/2012-03-13/Releasing_the_community_edition_of_SymbolSource)�˽�еĵ��Է�������

## �ؼ�����:

- 1 ����MySymbols��IIS��ȷ����ҳ�������ʡ�
- 2 �����ҳ��������ӣ�Run self-diagnostics�����鿴�Լ�״̬��
- 3 �����Լ�״̬����������
- 4 ��װwdk���Թ���(��ʾ����������2012R2����ʹ��wdk8.1_auto_download.exe)�����ز���װ��
- 5 VS�У����ߣ����ã����ԣ����棬����ѡ�����ý��ҵĴ��롱��ѡ������Դ������֧�֡�
- 6 VS�У����ߣ����ã����ԣ����ţ�����Symbols��������ַ������ҳ��ʾ�ĵ�ַ������http://{YOURSITEURL}/MySymbols/WinDbg/pdb��������һ��û������Ȩ�޵Ļ���Ŀ¼������C:\SymbolCache

## һЩע�����

- ����Լ��з���SrcSrvPath�����д���SrcSrvPath Configuration Test - Directory not found�������web.config�е�SrcSrvPath����ʵ�ʲ���ϵͳ�Ĳ�ͬ��·�����ܲ�ͬ��ע�ⰲװ����ȷλ��!
- ����Լ��з���push�д���NuGet Push Test - InternalServerError�������Գ��Խ�Ӧ�ó�����32λ���ã�Ȼ�����ԡ�

## some useful links

- [nuget.org](https://www.nuget.org/)
- [Creating symbol packages](https://docs.microsoft.com/en-us/nuget/create-packages/symbol-packages#referring-to-files-in-the-nuspec)
- [Releasing the community edition of SymbolSource](http://www.symbolsource.org/Public/Blog/View/2012-03-13/Releasing_the_community_edition_of_SymbolSource)
- [Is it possible to host both regular and symbols packages in a NuGet local feed on a network share?](https://stackoverflow.com/questions/45620764/is-it-possible-to-host-both-regular-and-symbols-packages-in-a-nuget-local-feed-o)
- [Serve up Debug Symbols for your NuGet packages? Heck yeah!](http://netitude.bc3tech.net/2015/01/12/serve-up-debug-symbols-for-your-nuget-packages-heck-yeah/)
