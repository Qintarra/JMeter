# JMeter

### Running a load test through the CLI

Open jmeter.bat in the *bin* folder (path to yout jmeter directory like **\apache-jmeter-5.5\bin**) //jmeter -? *options info*  
and run command:  
```jmeter -n -t 01.get.jmx```  
-n switch runs jmeter in non-GUI mode  
-t switch specifies the test file  
The test file should be in the same directory as JMeter (otherwise declare full file path)  

Note, that listeners are ignored when running through CLI (Only works through the GUI when creating/debugging)  
It's possible to capture all results information through the *.jtl* file, so in a command line add *-l filename.gtl* (-l switch specifies the log file)  
```jmeter -n -t 01.get.jmx -l getresults.gtl```  

