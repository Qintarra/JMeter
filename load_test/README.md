# JMeter

Endpoint: http://www.landonhotel.com/

### Running a load test through the CLI

Open jmeter.bat in the *bin* folder (path to yout jmeter directory like **\apache-jmeter-5.5\bin**) //jmeter -? *options info*  
and run command:  
```jmeter -n -t 01.get.jmx```  
-n switch runs jmeter in non-GUI mode  
-t switch specifies the test file  
The test file should be in the same directory as JMeter (otherwise declare the full file path)  

Note, that listeners are ignored when running through CLI (Only works through the GUI when creating/debugging)  
It's possible to capture all results information through the *.jtl* file, so in a command line add *-l filename.gtl* (-l switch specifies the log file)  
```jmeter -n -t 01.get.jmx -l getresults.gtl```  

You can use that .jtl file to graph the results within JMeter. Or you could ask JMeter to do most of that for you by creating a dashboard after running the test.  
Add two simple switches to your command line instructions:  
```jmeter -n -t 01.get.jmx -l getresults2.gtl -e -o getresults```  
-e generate report dashboard after load test  
-o output folder for report dashboard  

![CLI](/load_test/screenshots/CLI.png "CLI")

Then open the *index* file in a newly created *getresults* folder to view a dashboard and charts.

![index](/load_test/screenshots/dashboard.png "dashboard")

Settings example:

![Thread_Group](/load_test/screenshots/thread_group.png "Thread Group")

![HTTP_request](/load_test/screenshots/http_request.png "HTTP request")

![Timer](/load_test/screenshots/timer.png "Gaussian Random Timer")

![Summary_Report](/load_test/screenshots/report.png "Summary Report")
