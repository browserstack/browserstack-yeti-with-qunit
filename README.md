browserstack-yeti-with-qunit
============================

1) Clone the repository into your local folder.

2) Establish a local testing connection between your machine and BrowserStack. To do so, download command-line JAR file (Windows) or BrowserStackLocal (OS X or Linux) from
http://www.browserstack.com/local-testing#command-line . Once downloaded, setup the local testing connection using the following command:

```
./BrowserStackLocal -onlyAutomate -skipCheck SAMPLEKEY 10.100.100.116,9000,0
```

Replace SAMPLEKEY with your browserstack automate key.

3) To start testing sample.html on browserstack infrastructure, run :

```
yeti -wd-url "http://BSUSERNAME:SAMPLEKEY@hub.browserstack.com/wd/hub" -caps "browserName=chrome;platform=WINDOWS;browserstack.tunnel=true;browserstack.debug=true" sample.html
```

Replace BSUSERNAME with your browserstack automate username and SAMPLEKEY with your browserstack automate key.
Using the caps option, you can specify browserstack capabilities (More information at http://www.browserstack.com/automate/capabilities)