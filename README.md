# Mosquitto-MQTT-IoT-Platform-Series---7

![alt text](https://hackster.imgix.net/uploads/attachments/1563141/image_lRtXP52Vsm.png?auto=compress%2Cformat&w=740&h=555&fit=max)

In this project,  we will know and Understand MQTT protocol. Then implement and build a project to subscribe and publish on the public server of test. mosquitto. org. MQTT stands for Message-Queue-Telemetry-Transport, is a publish/subscribe protocol for machine-to-machine communication. This simple protocol, is easy to implement for any client. Termed as the Pub and Sub, both are used for same purpose but with different methods. 
Here, there are 2 sections - Publish and Subscribe. And then there is a middleman - Broker. Let us see in depth

IoT Devices play the role to collect sensor data and send to the cloud (broker). While PC/Server/Mobile devices play the role to monitor and receive the sensor data to be viewed - Here, IoT Device is a Publisher, and PC Devices are Subscriber.
[EXAMPLE] When a user1 publishes an image on social media, then only the user2 subscribed to user1 can view/receive the image. Here, the user1 is the PUBLISHER, user2 is the SUBSCRIBER, and the user1's account is the BROKER.
According to the above analogy, the image that is published is the data, that was transferred from user1 to user2 📤. And that is the exact scenario in an MQTT Pub/Sub model.
We have a more secure layer 🔒 to make sure the data is shared through a specific path, we call that 'topic', When user1 publishes data on topic, the subscriber automatically receives if already connected to the broker. Hence, the LOW latency.

![alt text](https://hackster.imgix.net/uploads/attachments/1563165/image_wR1RzdsgKV.png?auto=compress%2Cformat&w=740&h=555&fit=max)

Whenever there is a pub-sub model used as a message communication protocol, we require a broker that can transfer the information in the required device. This can be done by sending the message under correct topic.

Let us understand this -

A Broker is a runtime server (continuously running service), which can have 2 types of clients - Publisher (seller) & Subscriber (buyer)
For instance, when a seller sells a product through a broker to a buyer, then it is using the Broker's service to reach & find a secured buyer.
Similarly, when publisher publishes a piece of information, the data reaches to the subscriber through the Broker.
The broker is responsible for having specific storage space where it can expect data from the publisher to store temporarily and then send to the subscriber.
In the pub-sub MQTT, clients talk to each other through an MQTT broker.
There are many MQTT Brokers in the market. It is even possible to create our own broker, or use an open-source broker 'paho'.
For the current project, we shall first understand the mechanism and then watch a trial movement of data on Mosquitto MQTT Broker.

![alt text](https://hackster.imgix.net/uploads/attachments/1591014/image_5vIRzkcIF9.png?auto=compress%2Cformat&w=740&h=555&fit=max)

Now that we understand how MQTT works, let us use a cloud MQTT service and send data across the internet. In this article, we'll be using Mosquitto MQTT - test.mosquitto.org

Under the Server section, we can see different ports provide feature-separated servers. These servers act like channels for sharing data over the cloud. Let us understand it first -

MQTT Broker Port (default: 1883): This is the standard port used for MQTT communication. MQTT clients use I to connect to the Mosquitto broker and publish/subscribe to topics. It operates over TCP.
MQTT Broker SSL/TLS Port (default: 8883): This is the secure version of the MQTT broker port. It uses SSL/TLS encryption to provide secure communication between MQTT clients and the Mosquitto broker. Clients connect to this port to establish a secure connection.
WebSocket Port (default: 9001): Mosquitto also supports MQTT over WebSockets, allowing MQTT clients to connect to the broker using the WebSocket protocol. The WebSocket port is used for WebSocket-based MQTT communication.
WebSocket SSL/TLS Port (default: 9443): This is the secure WebSocket port used for encrypted WebSocket-based MQTT communication. It provides a secure connection using SSL/TLS encryption.

![alt text](https://hackster.imgix.net/uploads/attachments/1544797/pcbway_55Vl7NMRFG.JPG?auto=compress%2Cformat&w=740&h=555&fit=max)

You must check out [PCBWAY](https://www.pcbway.com/) for ordering PCBs online for cheap!

You get 10 good-quality PCBs manufactured and shipped to your doorstep for cheap. You will also get a discount on shipping on your first order. Upload your Gerber files onto PCBWAY to get them manufactured with good quality and quick turnaround time. [PCBWay](https://www.pcbway.com/) now could provide a complete product solution, from design to enclosure production. Check out their online Gerber viewer function. With reward points, you can get free stuff from their gift shop.

