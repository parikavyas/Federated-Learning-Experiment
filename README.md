# Federated-Learning-Experiment
Mini Experiment on federated Learning 

This is POC built to understand and experiment with the implementation of Federated Learning

Federated Learning Experiment 
To start with, we have 2 client servers and 1 central/main server in the network 
Steps to Run the FL Experiment: 
1.	Run “Device 1” using python app.py Server address: http://localhost:8001/
2.	Run “Device 2” using python app.py Server address: http://localhost:8002/
3.	Run “Secure Aggregator using python sec_agg.py Server address: http://localhost:8003/
4.	Run “Main Server” using python main_server.py Server address: http://localhost:8000/
5.	Training Local Models on individual client servers by navigating to - http://localhost:8001/modeltrain & http://localhost:8002/modeltrain
Once the Models are trained and saved locally, the server will be updated with the respective message. 
6.	Sending Status Signal to Main Server by navigating to http://localhost:8001/sendstatus & http://localhost:8002/sendstatus 
Once the client servers send the signal, there will be a response from the main server
7.	Sending Trained models to the secure aggregator server for model aggregation by navigating to http://localhost:8001/sendmodel & http://localhost:8001/sendmodel
8.	The secure aggregator will aggregate the model and build a global model http://localhost:8003/aggregate_models
9.	The secure aggregator will generate an aggregated model which is sent to the main server by navigating to http://localhost:8003/send_model_secagg
10.	This aggregated model is sent by the main server to the client servers by navigating to http://localhost:8000/send_model_clients
11.	Measure the model performances 
Next Steps: 
•	Experiment with model aggregation methods, and other Privacy enhancing technologies
•	App to simulate the devices and migrate the main server to Heroku or AWS 


Architecture Diagram 
![image](https://user-images.githubusercontent.com/28190165/163687540-b9997e00-c0cc-435d-b785-4326b9cb24f0.png)


