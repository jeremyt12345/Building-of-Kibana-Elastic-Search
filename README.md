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


