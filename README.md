# Assignment-21-Deep-Neural-Network
This is a repository for module 21 which explore in using deep neural network in creating a model with the data from the nonprofit foundation Alphabet Soup.
<h5>What's in the repository</h5>
In the repository are several files, where the first is the starting code and the three other script contains the three seperate model changes:<br/>
- Starter_code.ipynb - this is the main code which is written through jupyter notebook that contains tha script for creating the model as well as altering the model to see if it can be improved
- AlphabetSoupClarity.h5 - the saved model from the script (Start_code.ipynb)

-AlphabetSoupClarity_Optimisation1.ipynb - same jupyter notebook, with the adjusted model change (1)
-AlphabetSoupClarity_Optimisation1.h5 - saved model from the model change (1)

-AlphabetSoupClarity_Optimisation2.ipynb - same jupyter notebook, with the adjusted model change (2)
-AlphabetSoupClarity_Optimisation2.h5 - saved model from the model change (2)

-AlphabetSoupClarity_Optimisation3.ipynb - same jupyter notebook, with the adjusted model change (3)
-AlphabetSoupClarity_Optimisation3.h5 - saved model from the model change (3)

- ReadMe.md - information about the repository



<h1>Overview of the analysis</h1>
Overview of the analysis: Explain the purpose of this analysis.
The main purpose of the analysis revolves with creating a model through deep neural network that can be used to predict a value based on the weight of other factors from the previous recordings.
Essentially, the data file contains past records of organisation and the success rate based on the number of columns. Though the main highlighted column that is focused on are; the application type and classification.<br/>

The model is created through the use of standard scaler which is then applied to create the model. In the model, there are three hidden layers, each having a certain number of node, type of activation, and the for the 
first layer containing the number of input features in the model. These factors are then use to run the model with a set number of epoch based on the train y factor and the scaled train data. From there, the model loss value
and accuracy have been calculated to give the overall performance of the model.

<h2>Data Preprocessing</h2>
By reading the csv file, the columns that has been chosen to be the target for the model is: the calssification type which is successful (0 being a fail and 1 being a success).<br/>
All of the remaining variables/columns are shown below, and the two columns removed from the DataFrame are EIN and NAME as they aren't signifcantly related to the overall value.

![image](https://github.com/Nisloen/Assignment-21-Deep-Neural-Network/assets/134130254/4a1f1c8f-442d-4cd4-b368-cb84ea938fdc)

<h4>Compiling, Training, and Evaluating the Model</h4>
There are four different version of model, in order to find the best combination to achieve the best accuracy. The model summary are shown below with the known number of neuron, layer and activation functions.<br/>
![image](https://github.com/Nisloen/Assignment-21-Deep-Neural-Network/assets/134130254/be19f015-c50b-4636-a13d-97a605977820)
![image](https://github.com/Nisloen/Assignment-21-Deep-Neural-Network/assets/134130254/93a687ef-f452-46d5-ade1-2e9376e5a5b1)

This has two hidden layers, each containing 80 neruons with the relu activation function. Also an outer layer with 1 neuron and sigmoid activation function.<br/>
This is the first original model and the next three are variation attempt in creating a better model.<br/>

![image](https://github.com/Nisloen/Assignment-21-Deep-Neural-Network/assets/134130254/f7b16d1f-c2fe-47de-8747-07e9fffe0687)<br/>
![image](https://github.com/Nisloen/Assignment-21-Deep-Neural-Network/assets/134130254/256d4436-9661-4d13-abbc-42090b1ceb09)<br/>
This one is the same as before, but the second layer has half the number of neuron(40), this is because it may be that with less neuron, it wouldn't be overfitted and so may not be overwhelm. the model loss value has
decrease by 7 and the accuracy increased to 0.72.<br/>

![image](https://github.com/Nisloen/Assignment-21-Deep-Neural-Network/assets/134130254/332449b8-a030-4f00-8309-69d9ac595a7e)<br/>
![image](https://github.com/Nisloen/Assignment-21-Deep-Neural-Network/assets/134130254/45d2ea47-9517-48a1-8539-7db817b4f32d)<br/>
This one has one additionaly layer with the same number of neuron (80), the result shows that it has improve the accuracy, however it's not a hugh improvement.

![image](https://github.com/Nisloen/Assignment-21-Deep-Neural-Network/assets/134130254/7b96965f-3cde-44ab-af9a-641716e41adf)<br/>
![image](https://github.com/Nisloen/Assignment-21-Deep-Neural-Network/assets/134130254/6d76988f-046b-4511-a8e0-140e908277ab)<br/>
This one has the same setting type as the first model, the difference is the activation function which is set to sigmoid. This is mainly as the function graph are similar, the sigmoid smooth out in between which is believed
to provide the accuracy. Unfortunately, there isn't any improvement among the other models.<br/>


Out of all of the models, none of them have achieved greater accuracy than the second model attempy of 0.73. The process in how the model change are mainly one by one difference in order to really see the impact of the change
rather than completely altering the entire settings. Hence the three model attempt only had only onde differences, and at the end it didn't improve the model's accuracy. <br/>


# Summary
Out of the model, the best one happens to be adding an additional layer. This could be that it helps the model to refine in improving the data prediction. Although the model loss overall isn't great with the average of 0.57 which is
poor in predicting a single example. Though the average accuracy is 0.72, it can be precise in getting the results close to the line. This means that the model's weight across the feature may be the reason for the model's performance where
some of the columns value has a greater unnessecary weight compare to others.<br/>
If there's another attempt in improving the model, the weight would need to be adjusted.
