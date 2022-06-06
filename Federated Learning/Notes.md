
- hosting model and data on same device = centralized ML

Federated Learning
- instead of sending data to the cloud, send the ML model to our devices and train the models on our devices
- send back the updated model back to the server -> this is aggregated 
- devices communicate over Wi-Fi -> slower
- devices vary and have different data amounts and types
- non iid data 


How is this setting different from distributed training on GPU's?
- heterogeneity -> 
- communication -> all devices in GPU here are on the same network, whereas in federated learning, there is wifi communication
  
IID data = independent and identically distributed data = we sample from the same random variable each time
non IID data = primarily used for federated learning because every user has different data
  
  stochastic = having a random probability distribution or pattern that may be analysed statistically but may not be predicted precisely.

- FedAvg Loss:!
- 
[Screenshot from 2022-06-06 11-47-25](https://user-images.githubusercontent.com/91483133/172106044-6f80b991-3e02-43e2-8297-1b7d91620343.png)

