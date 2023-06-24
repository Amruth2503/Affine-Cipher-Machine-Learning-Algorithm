# Affine Cipher Machine Learning Algorithm

## Aim
The aim of this project is to generate a Machine Learning algorithm for the Affine Cipher.

## Affine Cipher
The Affine Cipher is a mono-alphabetic substitution cipher where each letter in an alphabet is mapped to its numeric equivalent (A to Z ~ 0 to 25). It is encrypted using a simple mathematical equation and converted back to its alphabetic equivalent.

```
p = (a * x + b) mod n
```

Here, `a` and `b` are constants or keys, and `n` represents the size of the alphabet (typically 26 when considering only the English alphabet).

## Introduction
The goal of this project is to create a machine learning algorithm for the Affine Cipher. The success of any machine learning algorithm relies on the availability of data to learn and train itself. Therefore, the first step is to create a dataset that follows the Affine Cipher.

## Data
To create the dataset, we randomly select words to encrypt and convert the data into information. We use the `random_word` module in Python to obtain random words.

The dataset consists of two lists: one containing the plain text of words, and the other containing the encrypted version of those words using the Affine Cipher.

To train the machine learning algorithm, we convert each string in both lists to its corresponding 8-bit binary representation using a binary encoder format.

Next, we consider the first 32 bits of each element in both lists and join them to form a 64-bit binary value. We create a dataframe with 64 columns and add a 65th column as the label/output, which is set to 1. Since we are using supervised machine learning algorithms, an output parameter is required.

We also convert the plaintexts into binary format, with each element having a length of 32 bits. We create a list of 64-bit elements, randomly assigning 0s and 1s. This matrix is then converted into a dataframe, with the label values set to 0.

Finally, we merge both dataframes row-wise, with labels 1 and 0, and shuffle the rows to obtain the complete dataset.

## Machine Learning
Before training the machine learning algorithms, we split the dataset into training and testing sets.

### 1. Random Forest Classifier
We use the Random Forest Classifier algorithm for training and testing the dataset.

### 2. Support Vector Machine (SVM)
We also utilize the Support Vector Machine (SVM) algorithm for training and testing the dataset.

## Comparison
After training and testing the dataset using both algorithms, we compare the accuracy of the models.

| Model                | Accuracy |
|----------------------|----------|
| Random Forest Model  | 99.87%   |
| SVM                  | 99.874%  |

## Inference
The accuracy rates obtained for both models are similar. Thus, we can either choose one of them or increase the volume of data and adjust the number of decision trees to improve the accuracy. It's worth noting that this model is specifically trained for the same key values. If different key values are used, the accuracy may be lower. Overall, this project demonstrates the creation of machine learning algorithms for the Affine Cipher.
