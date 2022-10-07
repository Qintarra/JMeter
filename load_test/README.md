# JMeter

### Running a load test through the CLI

Open jmeter.bat in the *bin* folder (path to yout jmeter directory like **\apache-jmeter-5.5\bin**) //jmeter -? *options info*
and run command:
```jmeter -n -t 01.get.jmx```
-n switch runs jmeter in non-GUI mode
-t switch specifies the test file
The test file should be in the same directory as JMeter (otherwise declare full file path)

