# JMeter

### Homework-1

Endpoint: http://5.75.203.123:5005

Load on 50, 250, 500 threads.

<details>  
<summary>HTTP Request</summary> 

1) http://5.75.203.123:5005/get_method  
request: GET  
name: string  
age: int  

2) http://5.75.203.123:5005/user_info_2  
request: POST  
name: string  
age: int  
salary: int  

3) http://5.75.203.123:5005/user_info_3  
request: POST  
name: string  
age: int  
salary: int  

4) http://5.75.203.123:5005/object_info_1  
request: GET  
name: string  
age: int  
weight: int  

5) http://5.75.203.123:5005/object_info_2  
request: GET  
name: string  
age: int  
salary: int  

6) http://5.75.203.123:5005/object_info_3  
request: GET  
name: string  
age: int  
salary: int  

7) http://5.75.203.123:5005/object_info_4  
request: GET  
name: string  
age: int  
salary: int  

</details> 

#### Running a load test through the CLI

Open **jmeter.bat** in the *bin* folder (path to yout jmeter directory like **\apache-jmeter-5.5\bin**) and run command:  
```jmeter -n -t hw-1.jmx```  
-n switch runs jmeter in non-GUI mode  
-t switch specifies the test file  
The test file should be in the same directory as JMeter (otherwise declare the full file path)  

Note, that listeners are ignored when running through CLI (Only works through the GUI when creating/debugging)  
It's possible to capture all results information through the **.jtl** file, so in a command line add *-l filename.gtl* (-l switch specifies the log file)  
```jmeter -n -t hw-1.jmx -l getresults_hw_1-50.gtl```  

You can use that .jtl file to graph the results within JMeter. Or you could ask JMeter to do most of that for you by creating a dashboard after running the test.  
Add two simple switches to your command line instructions:  
```jmeter -n -t hw_1.jmx -l getresults_hw_1-50.gtl -e -o getresults_hw1-50```  
-e generate report dashboard after load test  
-o output folder for report dashboard  

Also, you can use ```jmeter -?``` command for options info   

![CLI](/hw_1/screenshots/CLI_runs.jpg "CLI")

Then open the *index* file in a newly created [getresults_hw1-50](/hw_1/getresults_hw1-50) folder to view a dashboard and charts.  

![index](/hw_1/screenshots/dashboard.jpg "dashboard")  

hw-1.jmx opened in JMeter interface:    

![GUI](/hw_1/screenshots/GUI_tg.jpg "GUI")  

If you run a load test through the JMeter GUI, you can save the summary report into a *.csv* file, for example: [summary](/hw_1/hw_1-500_summary.csv)  
