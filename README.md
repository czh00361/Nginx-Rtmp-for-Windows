# Nginx-Rtmp-Windows
Refer to <https://qiita.com/estima5633/items/0fe1013734bd727ca11a>  Sorry Japanese HP

Mainly Step
Step1 Install Visual Studio 2010 with Microsoft SDKs
Step2 Down load
      Nginx and nginx-rtmp-module-master, pcre, openssl ,zlib.
      StrawberryPerl　64bit and then install.
Step3 Install MinGW.
Step4 Nginx module. make objs/lib folder
      unzip pcre, openssl, zlib, arut/nginx-rtmp-module and then move to objs/lib.
Step5 exec command prompt of Vsual Studio, c:\MinGW\msys.bat.
Step6 Input option on Nginx's configure.
        auto/cofigure --with-- .....
Step7 nmake -f objs/Makefile. and succsess nginx.exe.
