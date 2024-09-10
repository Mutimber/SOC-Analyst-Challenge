# SOC-Analyst-Challenge
## Objectives
- Obtain parcatical experience in 30 days
- Attain SOC skills
- 
## Day 1: Create a Logical Diagram
- Use draw.io
![image](https://github.com/user-attachments/assets/e53e99c1-d566-46a4-8a60-08fa086fbd56)
- Also available at: https://drive.google.com/file/d/1L3gU40TZzrhV33eyY3eX5-YQ_uN8TmAl/view?usp=drive_link

## Day 2: ELK Stack
- Understand what the ELK stack is and the benefits.
- Elasticsearch, Logstash, and Kibana >> ELK

**Elasticsearch** -> Indexer / search head
  - is a databases that stores logs - Windows, firewalls, etc.
  - Uses ES|QL - simple to learn and use
  - Also uses RESTful APIs and JSON

**Logstash** -> Heavy forwarder
- A free and open server-side data processing pipeline that ingests data from multiple sources, transforms it, and sends it to a 'stash.'
- Beats and Elastic agents collects telemtry - Universal forwarder.

**Beats:**
- File beats - logs
- Metric beats - metrics
- Packet beats - network data
- Winlog beats - Windows events
- Audit beat - Audit data
- Heartbeat beat -uptime

  Elastic Agent will largely be used in this challenge.

**Kibana** -> Web GUI
- Kibana allows use of web console to querry log stores in Elasticsearch instance.
- Kibana lens - build dashboards
- Data exploration
 Search data, create visualisations, and create reports & alerts

**Benefits of using ELK**
1. Centralised logging - meet compliance requirements & search data
2. Flexibility - custom ingestion
3. Visualisations - Observe information at-a-glance
4. Scalability - Esay to cinfigure to handle larger environments
5. Ecosystem - Many integrations and rich community
6. Many SIEMS are built on the ELK stack

## Day 3: ELK Setup
- Use vultr - free $300 credit which is enough for the project.
- Create a VPC 2.0 where the servers will be situated.
![image](https://github.com/user-attachments/assets/0574721e-7c82-45f7-b3bf-ae2a70d90a28)

- Deploy new virtual machines, retain default Type
![image](https://github.com/user-attachments/assets/6bbaac42-027a-4e18-b5af-9b2f03c8836b)

- Ensure location is same as the VPC network's - Amsterdam in this case
![image](https://github.com/user-attachments/assets/48340312-5b59-4f68-836c-a879356781db)

- Choose Image
- For ELK we use Ubuntue 22.04 LTS x64
![image](https://github.com/user-attachments/assets/4761dbd1-fb74-4146-bc83-998909180d69)

- Choose Plan
![image](https://github.com/user-attachments/assets/97fe8ad7-1eb4-467e-97e4-746bf581b7b8)

- In Additional Features, disable everything else apart from VPC 2.0
![image](https://github.com/user-attachments/assets/d062adf0-82e5-41eb-83a5-d557cfed7406)

![image](https://github.com/user-attachments/assets/3f2e3c9e-e328-416f-9c6b-e569bb059f2b)
- Name the server ELK and deploy
![image](https://github.com/user-attachments/assets/1ef6dc9f-24da-4175-a166-62aa8b4404aa)

- Now fully deployed
![image](https://github.com/user-attachments/assets/bb00d8f7-0d41-484a-b616-40f124aeecef)

- SSH into ELK from Windows powershell using the machine's IP and root password
![image](https://github.com/user-attachments/assets/fbfd83fe-51ba-45ca-bf07-167c9839978b)

- Now update the machine 

      apt-get update && apt-get upgrade -y 

- Press Enter when prompted with this screen to get the latter.
![image](https://github.com/user-attachments/assets/a3889d3d-1add-42b9-9ca6-4ccfb5a2e905)
![image](https://github.com/user-attachments/assets/46338691-3d08-4046-adf4-83b269943826)

- Now install ELK stack on the virtual machine.
![image](https://github.com/user-attachments/assets/f42a5011-dc1e-4c37-8b38-fdc7f3e4e7f4)

- Copy download link for Linux CLI

       wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.15.1-amd64.deb
![image](https://github.com/user-attachments/assets/c19d95c8-9647-43cb-b997-157b63fb1f16)

- Install Elasticsearch
![image](https://github.com/user-attachments/assets/ba131ad9-477f-4d23-95f3-db12ed3605ee)






