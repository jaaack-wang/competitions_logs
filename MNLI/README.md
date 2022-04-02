## Dataset

The dataset can be downloaded from: https://cims.nyu.edu/~sbowman/multinli/. 

The two competitions can be seen in the following two links:
	- https://www.kaggle.com/competitions/multinli-mismatched-open-evaluation/overview
	- https://www.kaggle.com/competitions/multinli-matched-open-evaluation/overview

## My submissions

- `bert-base-20220329`: The model was trained on the original train set and two dev sets together for 3 epochs. **Final test set accuracy**: Mismatched test score: 0.83995; Matched test score: 0.84748. 
	- Train with 10 epoches. Mismatched test score: 0.83527; Matched test score: 0.84269. Unconstrained overfitting!


- `bert-large-20220329`:The model was trained on the original train set and two dev sets together for 3 epochs (I also cut down the batch size so that the cloud computing environment I used could train the model). **Final test set accuracy**: Mismatched test score: 0.85355; Matched test score: 0.85718.
	- Train with 10 epoches. Mismatched test score: 0.85051; Matched test score: 0.85473. Unconstrained overfitting!


- `bert_base_20220331_with_val_earlystop`: bert base pretrained model with original dev sets kept for validations (that means, I did not separate the matched dev set and mismatched dev set for efficiency). I also used EarlyStopping callback (patience=3) to prevent overfitting. Turnt out that the model overfitted the train set in a way much quicker than when the dev sets were added to the train set, which may have something to do with the mismatched dev set, since this dev set comes with unseen text genres and thus can have different textual distribution. **The model performances declined a little bit**: Mismatched test score: 0.82126; Matched test score: 0.83095. 

- `bert_large_20220401_with_val_earlystop`: bert large pretrained model with original dev sets kept for validations (that means, I did not separate the matched dev set and mismatched dev set for efficiency). I also used EarlyStopping callback (patience=3) to prevent overfitting. **Mixed results**: Mismatched test score: 0.85061 (slight goes down); Matched test score: 0.86035 (surprising goes up!).
