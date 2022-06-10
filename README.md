# Neural Network Charity Analysis

A Deep Learning Algorith with TensorFlow

# Project Overview

The purpose of this project is to perform to Neural Networks Machine Learning algorithms in order to analyze how efficiently funds and donations from the foundation is used.

# Results:

### Data Preprocessing


* The Variable considered <strong> Target</strong> for the model :

After carefully investigating the dataset <code>IS_SUCCESSFULL</code> feature was used as target variable which is what our model will predict by utilizing rest of the features in the dataset. 

* The variables considered be the features <strong> Features</strong> for the model :
  * NAME *
  * APPLICATION_TYPE	
  * AFFILIATION	
  * CLASSIFICATION
  * USE_CASE
  * ORGANIZATION	
  * STATUS	
  * INCOME_AMT
  * SPECIAL_CONSIDERATIONS
  * ASK_AMT	

* The variables are neither targets nor features and removed from the input data

For 1st model , <code>EIN </code> and <code>NAME</code> was removed from the dataset before perform any feature enginering to establish our model .
However, after compiling the model and extract the accuracy report, it was discovered that keeping <code> NAME</code> as feature benefits for optimizing and increase accuracy of the model. 
Therefore, <code>EIN </code> was removed from the input data. 

### Compiling, Training, and Evaluating the Model

<table>
  <tr>
    <th> </th>
    <th> Initial Model  </th>
    <th>Optimized Model </th>
  </tr>
  <tr>
    <td> Number of neurons</td>
    <td> <ul>
        <li>1st Layer = 80</li>
      <li>2nd Layer = 30</li>
         </ul>
   </td>
    <td><ul>
        <li>1st Layer = 90</li>
      <li>2nd Layer = 50</li>
      <li>3rd Layer = 30</li>
       </ul></td>
  </tr>

  <tr>
   <td>Activation Function</td> 
    <td> <ul>
      <li>1st Layer = <code> relu</code></li>
      <li>2nd Layer = <code>relu</code></li>
      <li>Output Layer = <code>sigmoid</code></li>
         </ul>
    <td><ul>
      <li>1st Layer = <code> tanh</code></li>
      <li>2nd Layer = <code>relu</code></li>
       <li>3rd Layer = <code>relu</code></li>
      <li>Output Layer = <code>sigmoid</code></li>
         </ul></td> 
  </tr>
   <tr>
   <td> Number of layers</td> 
    <td>Layers = 2</td> 
    <td>Layers = 3</td> 
  </tr>
</table>

* Steps to try and increase model performance

  * 1- Use <code>NAME</code> as feature and create bin for it instead of removing it.
  * 2- Increase numbers of neurons for each layers. 
  * 3- Insert 3rd layers to the model, then removed it as it didnt make significant changes and decrease the model performance. Since we are using a relativly small dataset, it was not suggested to use more than 2 layers for the model .
  * 4- Changed activation function for 1st layer from <code>Relu</code> to <code>tanh</code>. In my opinion, <code>tanh</code>  normilizes the data better than <code> Relu</code>.
  * 5- No changes made in number of code>Epochs</code> as it would easly overfit the model .


<table>
  <tr>
    <th> </th>
    <th> Initial Model  </th>
    <th>Optimized Model </th>
  </tr>
  <tr>
    <td> Number of neurons</td>
    <td></td>
    <td></td>
    
  </tr>


Were you able to achieve the target model performance?
What steps did you take to try and increase model performance?
