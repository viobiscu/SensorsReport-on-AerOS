# SensorsReport-on-AerOS

The primary objective of this project is to migrate the existing monitoring solution existent at www.sensorsreport.com to the aerOS platform. By doing so, we aims to leverage the advanced features and functionalities offered by aerOS to enhance the overall system performance and reliability. The migration to aerOS will enable the company to optimize resource management, improve orchestration, and increase the resilience of their services. Moreover, aerOS's capabilities in supporting decentralized and scalable applications across the IoT edge-cloud continuum align perfectly with Synchro SRL's vision for the future.

This project is part of the Open Call 2 https://aeros-project.eu/open-call-2/
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


