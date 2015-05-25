[ESUG](http://www.esug.org) sponsored the initial release of this effort to develop a complete **xmlrpc** support for [Pharo](http://www.pharo-project.org). Thanks [ESUG](http://www.esug.org)!

If you or your company are interested in this project and want to help, can make a donation using the button of the article I wrote on my blog: http://germanarduino.blogspot.com.ar/2012/04/open-projects-financial-side.html

Check the project progress [here](ProgressReport.md).


## Install ConfigurationOfXMLRPC ##

**Xmlrpc** has a Metacello Configuration for Pharo / Squeak.
You can install one of several versions in the image where this configuration is loaded.
But first, you need to install this configuration.


### Pharo ###
```
Gofer it
	url: 'http://ss3.gemstone.com/ss/XMLRPC';
	package: 'ConfigurationOfXMLRPC';
	load.
	
(ConfigurationOfXMLRPC project version: '1.0-Beta3') load.
```


## Load XMLRPC ##

XMLRPC can be installed as the Client only (alone or with tests) and with Server component (also alone or with tests).

If you want the latest released version of XMLRPC, evaluate (by default the Client level is loaded)
```
ConfigurationOfXMLRPC project latestVersion load.
```

This is equivalent to evaluate
```
ConfigurationOfXMLRPC project latestVersion load: 'Client'.
```

If you want the Client and Tests, then evaluate
```
ConfigurationOfXMLRPC project latestVersion load: 'Client with Tests'.
```

If you want the Server (it requires the Client), evaluate
```
ConfigurationOfXMLRPC project latestVersion load: 'Server'.
```

If you want the Server (it requires the Client) and Tests, evaluate
```
ConfigurationOfXMLRPC project latestVersion load: 'Server with Tests'.
```

Or if you want ALL the packages, evaluate
```
ConfigurationOfXMLRPC project latestVersion load: 'All'.
```

But you can also load any version, not only the latest released version.
To install for example version 1.0.1, you'll evaluate one of:
```
(ConfigurationOfXMLRPC project version: '1.0-alpha1') load: 'Client'.
(ConfigurationOfXMLRPC project version: '1.0-alpha1') load: 'Client with Tests'.
(ConfigurationOfXMLRPC project version: '1.0-alpha1') load: 'Server'.
(ConfigurationOfXMLRPC project version: '1.0-alpha1') load: 'Server with Tests'.
(ConfigurationOfXMLRPC project version: '1.0-alpha1') load: 'All'.
```

The two last are equivalents.


### Upgrading ConfigurationOfXMLRPC ###
If you have an image with ConfigurationOfXMLRPC already loaded, and you want to use a version of XMLRPC that exists only in the newest ConfigurationOfXMLRPC package, you don't need to install ConfigurationOfXMLRPC as stated at the beginning, you can upgrade your current ConfigurationOfXMLRPC to the latest version with:
```
ConfigurationOfXMLRPC project updateProject.
```

And then install a new version as explained before.

When the installation is completed you can try to run some [Samples](Samples.md).

Thanks to Markus Fritsche and Christian Langreiter by their previous code in which I based my own.

Enjoy! (and report bugs, suggestions, comments).
