# tv-script-generation-udacity
Udacity project. Trains an RNN on 9 seasons of Seinfeld scripts and generates new scripts.

The original GitHub repo for this project can be found [here](https://github.com/udacity/deep-learning-v2-pytorch/tree/master/project-tv-script-generation).

## Architecture
RNN(
- (embed): Embedding(21388, 500)
- (lstm): LSTM(500, 512, num_layers=2, batch_first=True, dropout=0.5)
- (fc): Linear(in_features=512, out_features=21388, bias=True)
- (dropout): Dropout(p=0.3, inplace=False)
)

## Hyperparameters
- `sequence_length`: 5 
- `batch_size`: 256
- `num_epochs`: 10 
- `learning_rate`: 0.003
- `embedding_dim`: 500
- `hidden_dim`: 512 - Increased this again to see if it does better with a lower learning rate.
- `n_layers`: 2
  
- **RESULTS**
    - `Training Loss`: Fell to **3.35** after 10 epochs.
