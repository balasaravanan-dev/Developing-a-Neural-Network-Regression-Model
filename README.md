# Developing a Neural Network Regression Model

## AIM
To develop a neural network regression model for the given dataset.

## THEORY
Explain the problem statement

## Neural Network Model
Include the neural network model diagram.

## DESIGN STEPS
### STEP 1: 

Create your dataset in a Google sheet with one numeric input and one numeric output.

### STEP 2: 

Split the dataset into training and testing

### STEP 3: 

Create MinMaxScalar objects ,fit the model and transform the data.

### STEP 4: 

Build the Neural Network Model and compile the model.

### STEP 5: 

Train the model with the training data.

### STEP 6: 

Plot the performance plot

### STEP 7: 

Evaluate the model with the testing data.

### STEP 8: 

Use the trained model to predict  for a new input value .

## PROGRAM

### Name: BALA SARAVANAN K

### Register Number: 212224230031

```python
class NeuralNet(nn.Module):
  def __init__(self):
        super().__init__()
        self.fc1 = nn.Linear(1,8)
        self.fc2 = nn.Linear(8,10)
        self.fc3 = nn.Linear(10,1)
        self.relu = nn.ReLU()
        self.history = {'loss' : []}
    
  def forward(self,x):
    x = self.relu(self.fc1(x))
    x = self.relu(self.fc2(x))
    x = self.fc3(x)
    return x
```

### Dataset Information
<img width="429" height="609" alt="image" src="https://github.com/user-attachments/assets/d6f1cf33-c712-46bd-947c-8ee57e605746" />


### OUTPUT

### Training Loss Vs Iteration Plot
<img width="679" height="539" alt="image" src="https://github.com/user-attachments/assets/a49c416b-fdc1-4d48-812a-c850bdbfefc9" />


### New Sample Data Prediction
<img width="798" height="108" alt="image" src="https://github.com/user-attachments/assets/43a933af-f026-454e-9591-8e306d67f637" />

## RESULT
Thus, a neural network regression model was successfully developed and trained using PyTorch.
