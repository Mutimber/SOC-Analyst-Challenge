# Day 4
## Installing and Configuring Kibana
- Go to <a href="https://www.elastic.co/downloads/kibana">elastic</a> and select Debian distro as was the case with Elasticsearch in Day 3.
  ![image](https://github.com/user-attachments/assets/0d11ed1f-e27e-4218-8afb-4e4ad491af10)
- Copy download link and download using the ELK VM instance

      wget https://artifacts.elastic.co/downloads/kibana/kibana-8.15.1-amd64.deb

  ![image](https://github.com/user-attachments/assets/7af324bf-2c3d-4ce0-ac0f-bd2d32eea643)
- Install Kibana

      dpkg -i

  ![image](https://github.com/user-attachments/assets/8627c278-2efd-4d56-8b68-ec7a462b9027)

- Open configuration file

        nano /etc/kibana/kibana.yml
- Uncomment server.port and server.host and add the ELK VM public IP address
![image](https://github.com/user-attachments/assets/5154093f-6dd3-40b2-9265-da4217760d9f)
 
- Enable, start, and check status of kibana.service
![image](https://github.com/user-attachments/assets/e137e17e-826d-4521-bbf3-2d5a9fc630c8)

- Generate elasticsearch enrolment token for kibana

      cd /usr/share/elasticsearch/bin
  ![image](https://github.com/user-attachments/assets/3824957f-414d-410e-922d-9d35891e0832)

  ![image](https://github.com/user-attachments/assets/a61c2f14-a094-481a-958f-3206670efb72)

- Add TCP ports to the Firewall rule to allow connection to ELK on port 5601

  ![image](https://github.com/user-attachments/assets/7df0ea81-660e-4b13-9dbf-6d473e5f79d9)

  
