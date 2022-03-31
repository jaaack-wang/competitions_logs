## Dataset

The dataset can be downloaded from: https://cims.nyu.edu/~sbowman/multinli/. 

The two competitions can be seen in the following two links:
	- https://www.kaggle.com/competitions/multinli-mismatched-open-evaluation/overview
	- https://www.kaggle.com/competitions/multinli-matched-open-evaluation/overview

## My submissions

- `bert-base-20220329`: The model was trained on the original train set and two dev sets together for 3 epochs. Final test set accuracy: Mismatched test score: 0.83995; Matched test score: 0.84748. 
	- Train with 10 epoches. Mismatched test score: 0.83527; Matched test score: 0.84269. Unconstrained overfitting!


- `bert-large-20220329`:The model was trained on the original train set and two dev sets together for 3 epochs (I also cut down the batch size so that the cloud computing environment I used could train the model). Final test set accuracy: Mismatched test score: 0.85355; Matched test score: 0.85718.
	- Train with 10 epoches. Mismatched test score: 0.85051; Matched test score: 0.85473. Unconstrained overfitting!

