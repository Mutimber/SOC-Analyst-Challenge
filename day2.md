# Day 2: ELK Stack
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
