In this demonstration, I'll use one of my virtual machine to analyse the infamous wannacry ransomware on Any.run malware analysis platform.  

Background:  
WannaCry is a ransomware attack that occurred in May 2017, infecting computers worldwide. It exploited a vulnerability in Microsoft's Windows operating system, primarily affecting systems that had not installed a critical security update. WannaCry encrypted files on infected computers and demanded ransom payments in Bitcoin to decrypt them, causing significant disruptions to businesses, hospitals, and government agencies globally before a kill switch was accidentally discovered, slowing its spread.


First step, Logged onto one of my test VMs on my VirtualBox.  
From the browser, Will avigate to any.run which is a web-based malware analysis platform https://app.any.run/ which is publicly available to anyone.  

Next step is to get a malware file that is already submitted by other people.  
To do this, click on public report on the left.  

![image](https://github.com/user-attachments/assets/102f1bab-f019-4715-b503-fc04ae34d55e)  

Click on the filter icon on top right corner, this will help getting the malware file I want.  

![image](https://github.com/user-attachments/assets/3a1798bb-eb47-4b88-9636-4adfafa7afbd)

Once the filter page opens up, click the Verdict dropdown and choose Malicious option, type PE EXE, click on Search.  

![image](https://github.com/user-attachments/assets/082b0f58-82ff-46d0-98e5-e20ec71556ce)


This will filter in all results with only malicious files/malwares with high confidence.  
I'll utilize the search option at the top and look for infamous WannaCry, hit Enter  
From the results, will choose the Windows 10 option.  

![image](https://github.com/user-attachments/assets/11a215ab-1a91-44a5-b880-790891f3ab34)

Once clicked, the details page shows up with it's hash, IOC, type of threat and all other info about it. 
To get the sample file, Click get sample.   

![image](https://github.com/user-attachments/assets/d12d93f9-570d-438e-a744-12ae45215415)

This will download the sample file on my test VM, note the password. I'll need it to extract the compressed file later and upload to Any.run.

![image](https://github.com/user-attachments/assets/65ba7013-d00e-4d95-8570-81eb37313f8e)

Next, boot up a windows machine to run the virus on.  
To do this, click New analysis from the left menu, Upload the file that was downloaded earler, choose windows 10 64 bit, click Run a public analysis.  

![image](https://github.com/user-attachments/assets/3cc9b9d1-f76b-444f-b0f4-fa38c55c5113)

Once run on this machine, this has created 18 HTTP Requests, 107 Connections, 31 DNS requests, and detected 8 threats  

![image](https://github.com/user-attachments/assets/c7abe429-e053-4ccd-8e16-e632866ad5c8)

Clicking on each threat link comes up with that threat details.  

![image](https://github.com/user-attachments/assets/380c2474-e443-443c-b5d1-67ba1ca25291)

Clicking on more info brings up all the process information, timeline of each event including MITRE ATT&CK TTP (Tactics, Techniques, and Procedures)  

![image](https://github.com/user-attachments/assets/e2da01a1-2ab5-45b0-89bc-77a46d5839c6)

With behaviour of individual activity, file hash, IP, name etc.  

![image](https://github.com/user-attachments/assets/acd0866e-cfab-4e47-b694-07d4735e518d)

As well as all requests gone to outside world, URL, content etc  

![image](https://github.com/user-attachments/assets/f9f3672d-b532-4959-b3cb-8db9972c55e7)




