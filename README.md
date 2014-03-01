browserstack-yeti-with-qunit
============================

1) Clone the repository into your local folder. Install yeti

```
npm i -g yeti
```

2) Establish a local testing connection between your machine and BrowserStack. To do so, download command-line `JAR file` (Windows) or `binary file` (BrowserStackLocal for OS X or Linux) from BrowserStack [website] . Once downloaded, setup the local testing connection. For example, on OS X using BrowserStackLocal run the following command:

```
./BrowserStackLocal -onlyAutomate -skipCheck SAMPLEKEY 10.100.100.116,9000,0
```
Replace `10.100.100.116` with the `ip address` yeti server is listening on (To find that out, try yeti -s and notice the ip address it listens on. Press Ctrl+C to close yeti now)
Replace `SAMPLEKEY` with your browserstack automate key.

3) To start testing sample.html on Chrome browser (Windows platform) using BrowserStack infrastructure, run :

```
yeti -wd-url "http://BSUSERNAME:SAMPLEKEY@hub.browserstack.com/wd/hub" -caps "browserName=chrome;platform=WINDOWS;browserstack.tunnel=true;browserstack.debug=true" sample.html
```

Replace `BSUSERNAME` with your browserstack automate username and `SAMPLEKEY` with your browserstack automate key.
Using the caps option, you can specify your choice of `os`, `browser` and `device` versions (More information at [capabilities] page)

[website]:http://www.browserstack.com/local-testing#command-line
[capabilities]:http://www.browserstack.com/automate/capabilities
