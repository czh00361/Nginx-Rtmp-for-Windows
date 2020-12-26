# Nginx-Rtmp-Windows
Refer to <https://qiita.com/estima5633/items/0fe1013734bd727ca11a>.  Sorry Japanese HP.
Mainly Step.
Step1 Install Visual Studio 2010 with Microsoft SDKs.
Step2 Download under module.
      Nginx and nginx-rtmp-module-master, pcre, openssl ,zlib.
      StrawberryPerl　64bit and then install.
Step3 Install MinGW.
Step4 Nginx module. make objs/lib folder
      unzip pcre, openssl, zlib, arut/nginx-rtmp-module and then move to objs/lib.
Step5 exec command prompt of Vsual Studio, c:\MinGW\msys.bat.
Step6 Input option on Nginx's configure.
        auto/configure \
        --with-cc=cl \
        --with-debug \
        --builddir=objs \
        --prefix= \
        --conf-path=conf/nginx.conf \
        --pid-path=logs/nginx.pid \
        --http-log-path=logs/access.log \
        --error-log-path=logs/error.log \
        --sbin-path=nginx.exe \
        --http-client-body-temp-path=temp/client_body_temp \
        --http-proxy-temp-path=temp/proxy_temp \
        --http-fastcgi-temp-path=temp/fastcgi_temp \
        --http-scgi-temp-path=temp/scgi_temp \
        --http-uwsgi-temp-path=temp/uwsgi_temp \
        --with-cc-opt=-DFD_SETSIZE=1024 \
        --with-pcre=objs/lib/pcre-8.44 \
        --with-zlib=objs/lib/zlib-1.2.11 \
        --with-openssl=objs/lib/openssl-1.0.0e \
        --with-openssl-opt=no-asm \
        --with-http_ssl_module \
        --add-module=objs/lib/nginx-rtmp-module-master
Step7 nmake -f objs/Makefile. and succsess nginx.exe.
