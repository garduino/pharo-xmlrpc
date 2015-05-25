#samples of use of xmlrpc

## Snipplr samples ##
```
| url proxy r |

url := Url absoluteFromText: 'http://snipplr.com/xml-rpc.php'.
proxy := XMLRPCProxy new url: url.

r := proxy invokeMethod: 'languages.list' withArgs: #('Your snipplr key').

r := proxy invokeMethod: 'user.checkkey' withArgs: #('Your snipplr key').
r := proxy invokeMethod: 'snippet.list' withArgs: #('Your snipplr key' 'pharo').

"To get a snippet you don't need key, but the Snippet ID"
r := proxy invokeMethod: 'snippet.get' withArgs: #('41365').
```
The complete Snipplr xmlrpc API is on:
http://snipplr.com/blog/2006/07/06/snipplr-api/

## Flickr samples ##
```
| url proxy r |

url := Url absoluteFromText: 'http://api.flickr.com/services/xmlrpc/'.

proxy := XMLRPCProxy new url: url.


d := Dictionary new.
d at: 'name' put: 'FLICKRUSER'.
d at: 'api_key' put: 'FLICKRAPIKEY'.

r := proxy invokeMethod: 'flickr.test.echo' withStruct: d.
```


The complete Flickr xmlrpc API is on:
http://www.flickr.com/services/api/