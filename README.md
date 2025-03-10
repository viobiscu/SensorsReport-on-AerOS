# SensorsReport-on-AerOS

The primary objective of this project is to migrate the existing monitoring solution existent at www.sensorsreport.com to the aerOS platform. By doing so, we aims to leverage the advanced features and functionalities offered by aerOS to enhance the overall system performance and reliability. The migration to aerOS will enable the company to optimize resource management, improve orchestration, and increase the resilience of their services. Moreover, aerOS's capabilities in supporting decentralized and scalable applications across the IoT edge-cloud continuum align perfectly with Synchro SRL's vision for the future.

This project is part of the Open Call 2 https://aeros-project.eu/open-call-2/

This transition to aerOS not only promises to enhance performance and scalability but also positions Synchro SRL to stay ahead of technological advancements in the cold chain monitoring space, delivering even more value to its GXP-compliant clients.

## Expected results:
### Migration to aerOS Platform: 
The main goal is to successfully migrate Synchro SRL's cold chain monitoring system to the aerOS platform. This migration will enhance system orchestration and improve performance by leveraging aerOS’s advanced features.
### Improved System Reliability and Uptime: 
The transition to aerOS will enhance system reliability, a crucial aspect for GXP-compliant businesses. This ensures continuous system uptime, reducing the risk of downtime that could impact clients.
### Optimized Resource Allocation and Latency Reduction: 
aerOS will optimize resource usage across the IoT edge-cloud continuum, resolving issues like latency and GeoDNS inefficiencies, particularly with WiFi sensors using UDP protocols.
### Scalability and Future Growth: 
The system will become more scalable, allowing Synchro SRL to add future services and accommodate more devices without major changes, thereby supporting business growth.
Enhanced Real-time Data Management: Real-time data management will be maintained and improved, with a focus on ensuring data continuity during internet outages, using offline storage and MQTT communication.
These outcomes are substantiated, as they address specific current issues such as latency, connectivity, and scalability. The proposed improvements are based on the robust features of aerOS, which are designed to handle such challenges in IoT and edge-cloud environments. The migration will leverage aerOS’s proven capabilities, making the outcomes feasible and realistic.

## System Architecture Overview
The system will follow a microservices-based architecture with the following key components:

1. AerOS Edge Layer: Runs on Raspberry Pi and other IoT gateways.
2. Data Ingestion Layer: Handles sensor data collection and communication protocols.
3. Processing & Storage Layer: Manages real-time data processing, storage, and analytics.
4. Application & API Layer: Provides services such as alarms, reporting, and visualization.
5. User Interface Layer: Web-based dashboard for monitoring and administration.


## Sensor Communication & Integration
Each sensor type will be integrated as follows:

|Sensor Type	| Connectivity	| Protocol	|Processing Layer |
|------------:|---------------|-----------|-----------------|
|WiSensors	  |Direct UDP     |Proprietary|Listener & Parser|
|Termograf	  |Direct MQTT	  |Mosquitto  |	MQTT Subscriber |
|Modbus Device|	Raspberry Pi  |   VPN	    | Raspberry       |

## Edge Processing (AerOS)
### WiSensors Gateway: Parses proprietary UDP packets and forwards data via MQTT.
### Modbus Gateway: Raspberry Pi runs a Modbus client that reads sensor data and sends it via MQTT over a VPN tunnel.
### Termograf MQTT: Direct MQTT communication to a Mosquitto broker.


![image](https://github.com/user-attachments/assets/a9e3170c-deca-428d-95fb-d30941bec4a8)

