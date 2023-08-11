# NLP-project-Seinfeld-or-Friends

![Friends-vs-Seinfeld-Rivalry](https://github.com/sivanitzhaki/NLP-project-Seinfeld-or-Friends/assets/85245749/ec43f59a-7987-46c4-a5fe-2033381517d0)


I was provided with a dataset encompassing transcripts from both Seinfeld and Friends episodes. My objective is to construct a deep learning model capable of discerning whether a given line originates from an episode of Seinfeld or Friends.

## Data
The dataset contains total of 70405 scripts of Seinfeld and friends episodes.

* 39092 Friends Samples
* 31313 Seinfeld Samples

  ## Preprocessing

The following data preprocessing steps were executed:

* Lowercasing all letters.
* Eliminating special characters, newline characters, and stopwords.
* Employing stemming on the text.
* Subsequently, I conducted a train-test-validation split, employed tokenization using Keras' tokenizer, and transformed the data into sequences.

## The model
I used a fully connected 1D CNN model with an embedding layer and a dropout between the layers. In the FC layers I used the Relu activation function and in the last layer I used the sigmoid activation function for the classification.

| subject  | description |
| ------------- | ------------- |
| number of epochs  | 	5  |
| batch size  | 64  |
| Optimizer  | 		adam  |
| evaluation metric  | 	Accuracy  |


## Results
The accuracy score - 0.8118
### evaluate per actor:

| Actore	  | Accuracy Score |
| ------------- | ------------- |
| joey  | 	0.7  |
| phoebe  | 0.697  |
| elaine  | 		0.472  |
| chandler   | 	0.69  |
| kramer  | 	0.439  |
| monica  | 0.6727  |
| ross  | 		0.7157 |
| george   | 	0.411 |
| rachel  | 0.722 |
| jerry   | 0.417 |

We can see that joey,phoebe and rachel have the highest accuracy score. And george, kramer and jerry got the lowest accuracy scores.

## Vizualization
Let's see what a Friends Dialogue looks like using a word cloud:
![Friends Dialogue](https://github.com/sivanitzhaki/NLP-project-Seinfeld-or-Friends/assets/85245749/3ae2c7af-28ca-4cf6-b4a6-d0decd4903bb)

And a Seinfeld Dialogue looks like using a word cloud:
![Seinfeld Dialogue](https://github.com/sivanitzhaki/NLP-project-Seinfeld-or-Friends/assets/85245749/98b92911-b850-408d-8223-61bf857749aa)


