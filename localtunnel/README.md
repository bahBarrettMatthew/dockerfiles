localtunnel
===========
Node.js + [localtunnel](http://localtunnel.me/).

Usage
-----
**Note that this is only for forwarding HTTP(S) traffic.**

Enter the port to forward as the argument: `docker run -d --net host kaixhin/localtunnel <port>`.
Use `docker logs <container id>` to find out the address of your forwarded port.

Citation
--------
If you find this useful in research please consider [citing this work](https://github.com/Kaixhin/dockerfiles/blob/master/CITATION.md).
