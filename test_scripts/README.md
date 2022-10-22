# JMeter

### Recording and replaying the test script

1. Recording the test script:
- add the *HTTP(S) Test Script Recorder* from *Non-Test Elements* to your *Test Plan*
- change the *Target Controller* to *Test Plan > HTTP(S) Test Script Recorder*
- set up a proxy server (localhost, port: 8888)
- start recording some actions in your browser (go to http://2834008.youcanlearnit.net/ and navigate through it a bit and then stop recording)

2. Replaying the test script:
- add the *Thread Group* from *Threads (Users)* to your *Test Plan*
