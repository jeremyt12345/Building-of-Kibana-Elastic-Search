# Building-of-Kibana-Elastic-Search
Following a process to understand then Kibana/Elastic Search while understanding the whole process. My goal is to create a fake Hack The Box enviroment where I can ingest and analyze logs, runs tests, act as an attacker/defender by setting up an ubunto siem that will have the elastic agent and also spin up Kali linux and Windows VM.


Creating agent policy 

<img width="639" height="365" alt="image" src="https://github.com/user-attachments/assets/3a7db40c-7341-47ac-a233-928ead52a8fc" />

Then creating enrollement token

<img width="901" height="463" alt="image" src="https://github.com/user-attachments/assets/6bd223df-d5a8-48ef-9d3e-a661879a5dd2" />


Then installed successfully

<img width="863" height="626" alt="image" src="https://github.com/user-attachments/assets/99fa80d3-7b9e-4106-be53-c82f820aff69" />


Checking status of agent

<img width="1063" height="305" alt="image" src="https://github.com/user-attachments/assets/e250bf3c-f33b-4ff4-843b-f2708e2c7203" />


Now installing Windows Servor 2022 

<img width="788" height="688" alt="image" src="https://github.com/user-attachments/assets/cacb7afd-4c00-45e9-9419-431512d12571" />


Initally during the proxmox setup I chose the wrong network adapter so I couldnt connect to Elastic.com 

<img width="1016" height="311" alt="image" src="https://github.com/user-attachments/assets/3892a79d-0a59-4b2e-9a6a-1f03c7919124" />


Changed the network adapter and could hit it now getting this error. 

<img width="1523" height="841" alt="image" src="https://github.com/user-attachments/assets/797e1550-c6ee-451e-ae16-0d1041cb099b" />

Turns out it was just an error that was due to Elastic not being able to run on some old web browsers, due to it being on Windows Server it was running Intrernet Explorer. Installed chrome and now its running.

<img width="1682" height="518" alt="image" src="https://github.com/user-attachments/assets/2731b9e4-1488-41a6-8498-4f74d8779fbf" />


Then the process of installing the agent on Windows

<img width="1236" height="322" alt="image" src="https://github.com/user-attachments/assets/20d29e70-7256-49e3-a468-c7c5402e8d0b" />

Successfully installed agent

<img width="410" height="406" alt="image" src="https://github.com/user-attachments/assets/c1a186a1-7494-4c07-a0fe-6e5116979138" />


<img width="1732" height="276" alt="image" src="https://github.com/user-attachments/assets/c69af293-b60b-45a7-9d1c-72bd7110bd50" />


Now my task is to add policies in the Windows VM
<img width="1690" height="242" alt="image" src="https://github.com/user-attachments/assets/06e016c2-e35e-4b9d-9aa4-40fc5e515820" />

Next for Windows I want to download Sysmon for Windows


cd "$env:USERPROFILE\Downloads\Sysmon"

<img width="1187" height="436" alt="image" src="https://github.com/user-attachments/assets/acdcf32d-c485-4aa7-898f-e1d2bf849e1e" />

Confirmation of it being there/installed

<img width="1309" height="105" alt="image" src="https://github.com/user-attachments/assets/a92d2cfc-8aca-45f6-9d96-5d68c51575f8" />


Now adding policies for the Kali Linux machine 



<img width="1200" height="236" alt="image" src="https://github.com/user-attachments/assets/edfd085f-92f8-43ee-801f-381234e23781" />


After adding policies for linux I confirmed through terminal that they were running.

<img width="864" height="687" alt="image" src="https://github.com/user-attachments/assets/7a48d734-47ca-44eb-9e7c-f8ff6b5cf7e6" />


Done and finally ready to start simulating attacks and learn about them but first I wanted to go over my many issues setting this up and there were many.

My biggest issue was not understanding that all endpoint agents beloged on different VM's. To many who have alot of experience with virtualization and its concepts would know that easily but I literally struggled with that for 7 days. I was using A.I. and just simplying copying and pasting commands, while that can be helpful it makes things worse if you dont truly know what you're doing. 

So I took a step back and read documentation from the official Elastic website, looked at their troubleshooting section and also watch Youtube videos of others doing what I wanted. 


I dealt with expired tokens, the whole elastic site that I was hosting being down and having to reinstall that, learning how important Linux syntax is when writing commands down. 

This task helped me alot be more hands on with what I have been using in Hack The Box instead of just logging into their boxes, showed me what I dont know and also what I need to learn.



