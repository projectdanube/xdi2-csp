<a href="http://projectdanube.org/" target="_blank"><img src="http://projectdanube.github.com/xdi2/images/projectdanube_logo.png" align="right"></a>
<img src="http://projectdanube.github.com/xdi2/images/logo64.png"><br>

This is a configuration profile of the [XDI2](http://github.com/projectdanube/xdi2) server for 
hosting a dynamic number of XDI graphs. This is also known as the "cloud service provider" (CSP)
use case. The configuration should be considered a template and may be
adjusted according to one's needs.

### Information

* [Configuration](https://github.com/projectdanube/xdi2-csp/wiki/Configuration)
* [The registry graph](https://github.com/projectdanube/xdi2-csp/wiki/The-registry-graph)
* [Creating user graphs](https://github.com/projectdanube/xdi2-csp/wiki/Creating-user-graphs)
* [Deleting user graphs](https://github.com/projectdanube/xdi2-csp/wiki/Deleting-user-graphs)

### How to build

First, you need to build the main [XDI2](http://github.com/projectdanube/xdi2) project.

After that, just run

    mvn clean install jetty:run

Then use an XDI client to send XDI messages to the registry graph

    http://localhost:9301/registry

Or use an XDI client to send XDI messages to one of the dynamic XDI graphs

    http://localhost:9301/graphs/[=]!:uuid:1111

Or access the server's status page at

	http://localhost:9301/ (disabled in applicationContext.xml by default)

### Community

Google Group: http://groups.google.com/group/xdi2

IRC: irc://irc.freenode.net:6667/xdi
