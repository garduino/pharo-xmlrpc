# Progress Report #

## Coding Progress ##

  * April 1, 2011: All tests are green! A bit of code cleaning and the Beta is out!
  * March 28, 2011: Solved the failing tests about decoding structure when a dictionary is passed. Only 1 test remains failing.
  * February 6, 2011: Updated ConfigurationOfXMLRPC to load ConfigurationOfXMLSupport 1.1.7 and ConfigurationofKomHttpServer 1.0.7.
  * February 5, 2011: Tested in Pharo 1.2 - Must fix the Komanche in the installation by the Smalltalk os platformName.


## Next Steps ##

  1. Solve the remaining test failing and publish the first Beta version.
  1. Integrate the refactors sent by Sean P. DeNigris.
  1. Check and integrate the addition sent by Sean P. DeNigris.
  1. Evaluate Zinc support (at client level).
  1. Evaluate WebClient support (at client level, to integrate on Squeak also).
  1. Evaluate Swazoo support (at server level).


## ConfigurationOfXMLRPC ##

**ConfigurationOfXMLRPC** is on MetacelloRepository , documentation on
#workspace method.


## Names ##

I reorganized the **xmlrpc** packages, integrating the changes of Skrish, currently in PharoGoodies, renaming the packages in four categories:

XMLRPC-Client-Core

XMLRPC-Client-Tests

XMLRPC-Server-Core

XMLRPC-Server-Tests