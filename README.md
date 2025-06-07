<h1>Linux-Project-Monitoring</h1>

### [Pictoral Walkthrough Demonstration]

<h2>Description</h2>
In this lab we are going to walk through and show how the monitoring system works within Linix using the Centos7 distribution.
Monitoring is the process of collecting and analyzing data about the health and performance of your system. 
It is essential for preventing problems, identifying bottlenecks and ensuring that your system is performing at its best.
Poor system performance can have a number of negative consequences, including decreased productivity, reduced relaibilty, and increased
security risks. Proactive monitoring can help to identify and resolve problems before they cuase significant dusruptions.
 Some of the important keys to monitor are CPU utilization, Memory usage, Disk I/O, Network Traffic and Application Performance Metrics. 
<br />

<h2>Tools Used</h2>

-  <b>htop</b>
 - <b>vmstat</b>
 - <b>iostat</b>
 - <b>sar</b>

 <h2>Environments Used </h2>

- <b>Linux Centos 7</b>

<h2>Project</h2>

  <h3>In this project I would like show how various tasks are completed using different tools</h3>

 <h4>We will show how  regular system resource monitoring works.</h4>
    In this task we want to set up the necessary tools on servers for regular system 
    resource monitoring.

  <h4>Schedule Monthly Performance</h4>
    This will examine how to use a tool such as sar to make a monthly performance reporting.
    </br>


   <h2>Program Walk-Through</h2>
   <p align="center">
    Let examine the Top and the Systat Command <br/>
    <img src="https://imgur.com/EOQ7n7s.png" height="80%" width="80%" "/>
    <p align="center">We will start by by installing htop and sysstat in our Linux. This is done with the command "sudo yum install top systat". 
     Note: I have already installed these tools.<br/> 
     </br> 
     <p align="center"> Next, we will look will execute the TOP command.</br>
     <img src="https://imgur.com/CTyKENP.png" height="80%" width="80%" "/> 
     <p align="center"> Top provides insights about your system. In this example, the top is displaying info about the total Memory and Swap Usage.        (ie:KiB Mem and Kib Swap). You can also see the load average and the system uptime. The main tab in black displays the Process ID (PID); The         user running the process;The virtual memory (VIRT);The reserved memory,CPU and Memory utlilzation (MEM%), and
      Command label you should see the running command or process.
      If you and on a system running top and you notice a process consuming memory, what should you  do?
      First ask yourself whether this is a normal process. If it is you must investigate  why it is consuming so much memory. 
      Does this process or service need optimization to consume less memory.
      Note : If you observe and process consuming too much memory, there should be a spike, and if you see a process consuming to much swap                something is wrong with that process. The system  should terminate the process automatically to protect itself.
      But if the process re-starts or recreates itself automatically, the system will eventually crash.<br/>
      <p align="center"> The Kill Commnand</br>
            <img src="https://imgur.com/7N9LCev.png" height="80%" width="80%" "/> 
             <p align="center"> Therefore you must kill that process. How to go about doing that is but using the command pkill or kill and the 
                                name of the process. Then go back to the "top" table to see whether the process is still  there and whether the                                      memory and swap has been restored to normal levels. 
             <p align="center"> Next, lets examine detecting memory issues.</br>
             <img src="https://imgur.com/ogOZPnc.png" height="80%" width="80%" "/>
             <p align="center">To detect memory issues on a system execute the command sudo cat /var/log/messages | grep memory. if you observe the                                  words "out of memory" in the output, know that your process is consuming memory and the system terminated a process                                  to protect itself. The output will show the process which caused the out of memory issue and has been terminated.
              <p align="center"> The VMSTAT command</br>
              <img src="https://imgur.com/CXJSEnQ.png" height="80%" width="80%" "/> 
              <p align="center">The vmstat command provides information on memory, swap, input, output, system and cpu.  First lets execute "vmstat"                                 From the output you will observe information about memory,  the swap, the input/output, the system and the cpu.
                                 To know which options you can add to the vmstat is by using the command vmstat --help
              <p align="center"> The IOSTAT command</br>  
               <img src="https://imgur.com/6a4SOrT.png" height="80%" width="80%" "/>
               <p align="center">This command shows information about the Linux kernel; today's date; The system  architecture, the number of CPUs,                                   and the average cpu, iostate allows displays the device  attached to their system; transactions per second (tps)                                     (which is how many read and write   operations per second); the amount of read per second (kb_read/s), the amount                                    of write per secound (kb_wrtn/s); and the total read and writes per second. <p align="center"> 
                                 The df -h command</br> <img src="https://imgur.com/Oi6iugS.png" height="80%" width="80%" "/>
                <p align="center"> Now to check the available devices attached to the system execute the command df -h. Here you will see                                               /dev/mapper/centos-root.. To allow you to get information on this machine type iostat. Using IOSTAT can help you                                      identify a storage problem because reading and writing can affect the performance. 
                <p align="center"> The SAR command</br> 
                <img src="https://imgur.com/Ox3axCH.png" height="80%" width="80%" "/>
                <p align="center">This generates or reports CPU utilization, input/output and other system statistics. To execute SAR use the                                          command "sar". From the output you can see that sar shows the current version of your Linux, the hostname, the                                       date, the system architecture and the number of CPUs.
                <p align="center"> SAR example</br>
                <img src="https://imgur.com/IjpBF1d.png" height="80%" width="80%" "/>
                <p align="center">If you notice in the last time of the SAR example the idle percent drops down and at the same time the system                                       percentage shows at spike. When you see something like this, this indicates that there was a problem at 7:40.04                                     AM. When you see something like that you need to investigate what happen at that time.
                <p align="center"> Other Options within SAR</br>
                <img src="https://imgur.com/VvjMQQI.png" height="80%" width="80%" "/>
                <p align="center">To check out other options that you can use with SAR you can you the command SAR --h.  If you wanted SAR to                                         generates old metrics it collected you can use the command sar -A. SAR will generate CPU,memory storage, and old                                    metrics is collected.
                                  To find where sar log files and reports are stored execute the command  ls /var/log/sa sar or you can use ls                                        /var/log/sa -l By using the command ls /var/log/sa -l you can match of file names to the dates in which 
                                  they were created. There are other things you can use the command for with options. This is too extensive 
                                  for this project so further self study is important to full understanding all aspects of this subject

               
      
     

      




     


      
 
     

         

       
    
    
     
  
  
