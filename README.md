# Kali-stuff
Problems and fixes
#HydraFW
```
hydrafw/scripts# python get-pip.py 
Traceback (most recent call last):
  File "get-pip.py", line 17474, in <module>
    main()
  File "get-pip.py", line 17466, in main
    bootstrap(tmpdir=tmpdir)
  File "get-pip.py", line 17406, in bootstrap
    import pip
  File "/tmp/tmpjJAPLk/pip.zip/pip/__init__.py", line 11, in <module>
  File "/tmp/tmpjJAPLk/pip.zip/pip/vcs/mercurial.py", line 9, in <module>
  File "/tmp/tmpjJAPLk/pip.zip/pip/download.py", line 22, in <module>
  File "/tmp/tmpjJAPLk/pip.zip/pip/_vendor/requests/__init__.py", line 53, in <module>
  File "/tmp/tmpjJAPLk/pip.zip/pip/_vendor/requests/packages/urllib3/contrib/pyopenssl.py", line 70, in <module>
AttributeError: 'module' object has no attribute 'PROTOCOL_SSLv3'
```
fix:
```
/usr/lib/python2.7/dist-packages# ls -la | grep -si openss
drwxr-xr-x   3 root root   4096 Mar 10 19:09 OpenSSL
drwxr-xr-x   2 root root   4096 Feb  1 10:26 pyOpenSSL-0.15.1.egg-info
/usr/lib/python2.7/dist-packages# rm -rf OpenSSL
/usr/lib/python2.7/dist-packages# rm -rf pyOpenSSL-0.15.1.egg-info
```
## autoreconf / autoconf
```
# ./autogen.sh 
./autogen.sh: 2: ./autogen.sh: autoreconf: not found
# apt-get install autoconf
```
