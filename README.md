# AI-Smart-Agriculture-with-On-Board-Processing
# (Distributed Machine Learning for Crop Weed Detection through Federated Learning and Convolutional Neural Networks)
## Objective:

The objective of our project was to detect various types of weeds using frameworks like tensorflow, keras and algorithms like federated average learning using images from the chosen dataset, "DeepWeeds: A Multiclass Weed Species Image Dataset for Deep Learning" published with open access by Scientific Reports: 
https://www.nature.com/articles/s41598-018-38343-3  

It is an enormously vast dataset consisting of 17,509 images captured from eight different weed species native to the Australian continent in situ with neighbouring flora. The reported weed species are local to pastoral grasslands across the state of Queensland in Australia. They include: "Chinee apple", "Snakeweed", "Lantana", "Prickly acacia", "Siam weed", "Parthenium", "Rubber vine" and "Parkinsonia". The images were collected from weed infestations at the following sites across Queensland: "Black River", "Charters Towers", "Cluden", "Douglas", "Hervey Range", "Kelso", "McKinlay" and "Paluma".

## Need for the project:

Agriculture has always played an important role in the country’s economic sector making automation in agriculture an emerging subject and the main concern, reasons
being increased food demand, population growth, poverty etc. Various technologies like IoT, AI/ML are being introduced, studied and deployed because traditional methods
are no longer sufficient to meet the ever-increasing needs.
 
AI technology and the algorithms can make predictions from various departments over weather conditions (eg. Rain-fed cultivation), other agricultural conditions like land quality, groundwater, crop cycle, pest attack, weed detection etc. Data extracted from AI-driven sensors help in enhancement of production.  

## Work Done:

As a small part of this enormously broad topic and project, we utilized unified averaging calculation to predict and detect types of weeds. This takes loads from the circulated display and is sent to a server that would take normal of the loads and then is sent back again to heterogeneous gadgets. We also reviewd quite a bunch of papers as a part of the research -  - a few to name. We were able to compare the efficiency, output, and accuracy rates for different algorithms that had been used in the papers. 
We decided to use Federated Learning that allows the model to learn from the data rather than the data learning from the model to get weights and losses.

## Federated Learning:
Federated Learning is a sophisticated way to connect machine learning models to these disparate data sets, regardless of where they are stored, and, more crucially,
without violating privacy rules.Federated Learning takes the model to the data rather than the data to the model for training. 

They (clients) each get the weights of the current global model from the host, then train it on their own data to produce new parameters, which are then sent back to the server for compilation. This communication cycle continues until a predetermined epoch number, or an accuracy criterion is met. The compilation is essentially an averaging process in the Federated Averaging Algorithm. 

![image](https://user-images.githubusercontent.com/91736056/176937589-78da6e24-8320-4566-af34-6254193ea7d8.png)

The above equation estimates each client's weight parameters based on the loss
values reported for each piece of data they trained with. Later, each of those factors is
scaled and added up component-by-component on the left. The quesdo code is
available below.

![image](https://user-images.githubusercontent.com/91736056/176937714-b806d6ca-d570-4399-ba23-8eb74718c7ca.png)

Unlike conventional techniques unified learning includes every one of the information stockpiling and handling exercises on the PC and takes out the
requirement for distributed storage administrations. This breaking down of AI from portable distributed storage administrations permits the utilization of nearby models on cell phones to make expectations by taking models to the cloud. 

In past frameworks the information from customers were shipped off the server where
the AI model was prepared when that information was taken care of. In the proposed framework we are utilizing unified averaging calculation which would simply take the
loads from circulated display and send it to the server which would take normal of the loads and send it back to the heterogeneous gadgets and prepare on every gadget
proceeds without move of information in this manner expanding protection and security.

The dataset is divided into a given number of respective clients. It is followed by preprocessing of data like image normalization, rescaling, rotation, zoom, orientation, change in color scale and model-specific preprocessing, if needed. For each client, test images are common while the training set is divided as per number of clients. 

## Optimizer, Loss Function, Weight Averaging and Metrics:

For our model, we intend to use Adam as the optimizer function and Sparse Categorical cross entropy as the loss function. All the clients are prepared parallely with a novel dataset given to them. Then, we utilize the combined learning for preparing our client models for a given number of correspondence adjusts. Here we extracted the weights of each model and allotted the mean normal of the weights to each show and trained again in every correspondence round.

We used Adam Optimizers since it was more appropriate for larger datasets. Adaptive Moment Estimation is an approach for optimising gradient descent algorithms.

![image](https://user-images.githubusercontent.com/91736056/176939083-d6b7b622-d1c3-45fc-b8f2-7dda922e3c82.png)

![image](https://user-images.githubusercontent.com/91736056/176939108-56550d64-f8aa-4f8f-accf-6bde02dfa4fe.png)

Since we are using the softmax function on the Resnet model, a corresponding loss function cross-entropy-loss is adopted. It is used in classification problems when we
want to minimise the likelihood of a negative class by maximising the estimated return of some function on our training data. It is used to compute the difference between two probabilities assigned by the model to classes.

![image](https://user-images.githubusercontent.com/91736056/176939173-1b8b53e7-902b-48a5-a394-717f1047a57e.png)

Weight scaling function determines the percentage of a client's localized training data compared to the total training data collected by all clients. We first determined the client's batch size and utilised it to determine the amount of data points and then we scale the global weights to the local environment. 

![image](https://user-images.githubusercontent.com/91736056/176939314-7e6870c0-9e98-4073-ba3e-52b4f6fc65f2.png)


## Our Work Flowchart:

![image](https://user-images.githubusercontent.com/91736056/176938244-20f45eea-b8ed-4358-bfe2-43722eb999be.png)

## Result :

Following are the confusions matrices and Global Losses for the model with complete and reduced datasets: 

![image](https://user-images.githubusercontent.com/91736056/176938610-f8761d4f-b999-4374-bd55-e5b5174a1089.png)

![image](https://user-images.githubusercontent.com/91736056/176938656-7ba0fcc3-98aa-408f-9f3f-75e0b2f7f652.png)

![image](https://user-images.githubusercontent.com/91736056/176938696-89c21b76-063d-461e-9905-087c9dc42fec.png)

![image](https://user-images.githubusercontent.com/91736056/176938717-cd2c3652-7b21-4a73-ba61-8604a2f60058.png)


## Conclusion:
The preceding analysis can be applied to our investigations in order to create an optimal weed identification system. By doing trials on sensor data, we can train and
fine-tune our learning parameters to improve accuracy and repeatability. In addition, we can derive numerical conclusions that allow us to employ an algorithm or activation function that is more efficient than models that may be computationally more expensive. The developed formulation can be used to compute system parameters. Distributed Machine Learning can be implemented for Crop Weed Detection through Federated Learning and Convoluted Neural Networks after considering all pitfalls and advantages.








