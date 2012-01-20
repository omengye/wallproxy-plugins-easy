这是一个wallproxy-plugins的简化版，旨在在无UI的模式下运行代理，
更加详细的描述见此 http://code.google.com/p/wallproxy-plugins/

windows 的环境配置为

Python-2.7.2 http://www.python.org/getit/

pyOpenSSL-0.13.winxp32-py2.7 http://pypi.python.org/pypi/pyOpenSSL

pycrypto-2.4.1.win32-py2.7

其中的 pycrypto-2.4.1.win32-py2.7.exe 为使用VS编译在 https://www.dlitz.net/software/pycrypto/ 
上的 pycrypto-2.4.1.tar.gz 而来

1. src; proxy; startup 均由wallproxy-plus_V1.0.8_Memono_Mod.7z 直接 copy 得来

2. crypto 及 OpenSSL 文件夹由7zip解压缩 wallproxy-plus_V1.0.8_Memono_Mod.7z 中的proxy.exe，
提取出OpenSSL和Crypto，并用 win-patch.py 修改而得

使用

按顺序安装 Python pyopenssl pycrypto
如何设置密码请见 http://code.google.com/p/wallproxy-plugins/wiki/ConfigClient 
设置之后将该 app 禁用一下再启用以清空缓存
在 proxy 文件中填入自己的GAE ID，密码(AES-CBC-32模式下)
双击 startup.py 即可运行并生成cert证书目录

Linux (archLinux) 下需要的安装包有

python2
python2-openssl
pycrypto

随后运行 python2 startup.py 即可