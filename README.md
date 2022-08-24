
<h3 align="center"> Womanium Quantum Hackathon 2022 </h3>
<h2 align="center"> Random Number Generation Using Boson Sampling by Orca Computing</h2>

<p align="center">
  <img style="float: right;" src="LogoNarrow.png" width="350">
</p>


|   **Name**| **Soubhadra Maiti**                      | **Owais Ishtiaq Siddiqui** | **Suzielli Mendonça** | **Zeynep Kılıç**          |
|----------------|------------------------------------------|----------------------------|-----------------------|---------------------------|
| **Discord ID** | Soubhadra_Maiti#2170                     | owaisishtiaqsiddiqui#4549  | Suzielli#5080         | paperfrog#7510            |
| **GitHub ID**  | SouPhyzics                               | owaisishtiaqsiddiqui#4549  | Suzielli-m            | paperfrogs                | 
| **E-mail**     | soubhadra.maiti@students.iiserpune.ac.in | owaisishtiaq15@gmail.com   | suzielli@usp.br       | zeynepkilic3663@gmail.com |   


### Team Name: _Random Qubits_
#### Pitch Presenter: _Owais Ishtiaq Siddiqui_

Our Solution	 

In this challenge we had to build some kind of application that could generate random numbers using a quantum computing device called a boson sampler.  

We were able to simulate a quantum random number generator using Strawberry fields package. Firstly, we have defined a function called qrng_func(). In the function we define the number of nodes and initializes Fock states. Rotation gates are applied to each mode and the resulting rotation in the phase space occurs in the anticlockwise direction, with angle 
𝜙
𝜙
 
. 

The array of Beamsplitter by using the BSgate operator with arguments (
𝜃
𝜃
 
,
𝜙
𝜙
 
)  

Transmitted amplitude is represented by cos
𝜃
𝜃
 
 

Reflection amplitude is given by 
𝑒𝜄𝜙sin𝜃
e𝜄𝜙sin⁡𝜃
 
. 

The rotation gate and beamsplitters parameters are chosen by default (i.e. 
𝜋4
𝜋4
 
). 

 

After generating the samples, we apply the post-processing part, which is the Von Neumann Correction. Random numbers are directly obtained from the Boson Sampling to get a completely uniform and unbiased distribution [1]. Steps involved in Boson Sampling requires the comparison of two Samples. If the digits were the same, we wouldn’t keep them. Otherwise, we would have two options: 

if we had the digit 1 in the first sample and the digit 0 in the second, the final result would be the digit 0 

 

if we had the digit 0 in the first sample and the digit 1 in the second, the final result would be the digit 1. 

All the codes were implemented in Python programming language using the Strawberry fields library. We have simulated the samples both locally and in the Xanadu quantum computer. The output of our program is a sample with 8 random bits. 

Finally we tested our samples u 

 

 

Possible Application 

In machine learning models, when learning the parameters of a prediction function and testing it on the same data is a methodological mistake: a model that would just repeat the labels of the samples that it has just seen would have a perfect score but would fail to predict anything useful on yet-unseen data. This situation is called overfitting. To avoid it, it is common practice when performing a (supervised) machine learning experiment to hold out part of the available data as a test set. 

One way of performing this test is by using the Scikit-Learn Python library. Inside this library, there is a module called train_test_split, which splits arrays or matrices into random both train and test subsets. In our solution, we propose using the random sample we have generated to split the dataset into the abovementioned subsets. To do so, the program would use the random position of zeros  

and ones to label the data in the dataset as “test” or “train”. For instance, one could define that the zeros represent a test data and the ones represent train data. Let’s consider the following dataset  

 

0 

1 

2 

3 

4 

5 

6 

7 

Table 1: A dataset example 

1 

0 

1 

0 

0 

1 

1 

0 

Table 2: A random sample example 

 

 

All the numbers from the dataset example marked in the yellow color would be chosen to be in the test subset (according to the random sample) and all the numbers marked in the green color would be in the train subset. 

Our proposal stands out as a fast and simple way of using real random numbers in a well-known machine learning model. In order to implement that, one would only have to generate the random sample (as shown in the Jupyter Notebook attached on this repository), export and import it to the model desired. 

 

 

References 

[1] Shi, J., Zhao, T., Wang, Y., Yu, C., Lu, Y., Shi, R., ... & Wu, J. (2022). An Unbiased Quantum Random Number Generator Based on Boson Sampling. arXiv preprint arXiv:2206.02292. 
