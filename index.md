# Tips!!
hello world!!
## WSLからSSHの接続でX Forwardingを行った際に接続できない場合
###通常のlogin先からのX Clientの起動
```
+------------------------+    +--------------------------------+
| Remote Host X Server   |    | Local Host X Server            |
| X Client               +----+ inet          unix             |
| DISPLAY:X tcp:6000+X   |    | tcp:6000+X -> /tmp.X11-unix/X0 |
+------------------------+    +--------------------------------+
```
VcXsrvを

参考.
http://luozengbin.github.io/blog/2014-06-21-%5B%E3%83%A1%E3%83%A2%5D%E3%83%AA%E3%83%A2%E3%83%BC%E3%83%88x%E3%81%AE%E6%8E%A5%E7%B6%9A%E6%96%B9%E6%B3%95.html
