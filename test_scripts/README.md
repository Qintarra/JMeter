# JMeter

### Recording and replaying the test script

1. Recording the test script:
- add the *HTTP(S) Test Script Recorder* from *Non-Test Elements* to your *Test Plan*
- change the *Target Controller* to *Test Plan > HTTP(S) Test Script Recorder*
- set up a proxy server (localhost, port: 8888)
- start recording some actions in your browser (go to http://2834008.youcanlearnit.net/ and navigate through it a bit and then stop recording)

2. Replaying the test script:
- add the *Thread Group* from *Threads (Users)* to your *Test Plan*
- also add to *Test Plan* from *Config Element* next elements: 
    HTTP Header Manager, 
    HTTP Cookie Manager, 
    HTTP Cache Manager
- select the root request in *HTTP(S)Test Script Recorder*, go to the *Advanced* tab and mark the *Recieve All Embedded Resources* checkbox
- go to script recorder and select the steps that you want to rerun
- copy them and paste them to the *Thread Group* by right-clicking on it
- now you can delete the *HTTP(S)Test Script Recorder* to tidy up a test a little bit
- add a listener *View Results Tree* to the *Thread Group* 
- replay the test script by clicking the *run* button

![Replaying](/test_scripts/screenshots/test_script_replaying.jpg "test script")

### Logining In

1. Record your session by login in with a valid username and password:
- create *HTTP(S) Test Script Recorder* and start recording
- open http://2834008.youcanlearnit.net/account/
- enter the test username *mikesmith@twotreesoliveoil.com* and password *mikeisgreat123* and click the *Sign In*
- stop recording

2. Preparing a test
- Add the *Thread Group*
- find and copy the POST command from *HTTP(S) Test Script Recorder* to the *Thread Group*
- add a listener *View Results Tree* to the *Thread Group* 
- you can delete the *HTTP(S)Test Script Recorder* 
- run the test

3. Result
- you can now dig into this result: go into *Response data* and see the HTML that it came back with  
- by using the Text dropdown, you can select HTML to give yourself a better view of what has been returned

![Logining In](/test_scripts/screenshots/logining.jpg "test result")

### Data-driven testing with .csv file

1. *Thread Group* > *Config Element* > *CSV Data Set Config*:
- browse your *CSV* file location in the *Filename* field
- in the *Variable Names* you can mirror the headings for the columns of the *CSV* file
- change *Ignore first line* dropdown to *True* (allows JMeter to ignore the first row of the *CSV* file)

2. Back to the request and replace the email and password that are on this request for the following values:
- ${username}
- ${password}
*Note that is a curly braces*

3. Open *View Results Tree* and run the test
