**SE23MAID015-A3.zip** file consists of 4 folders named codes, data, models, word_vectors.
- codes folder consists of 2 files fastText_code.ipynb & word2vec_code.ipynb
- data folder consists of dataset "aclimdb"
- model folder consists of 2 files fasttext_model.npy and word2vec_model.npy(files where trained models are stored)
- word_vectors folder consists of 2 .txt files - word_vectors_fastText.txt and word_vectors_word2vec.txt which consists of word embeddings

**How to execute .ipynb files**
1. open any one of the file say for one ex.fastText_code.ipynb which consists of 2 codes in 2 differnt cells.
2. First code is the one which is used to generate the word vectors from fastText model. Those word vectors are stored in a file named "word_vectors_fastText.txt" and the model is stored in a file "fasttext_model.npy".
3. The second code is to train the rnn model for sentiment classification task using the pre-trained model and word embeddings/word vectors. Thernn model is trained and then  tested using the test data and loss is calculated after every epoch.
4. The Evaluation metrics like Accuracy, precision, recall and f1-score is printed.

The same method is followed for the other model like word2vec.

**Paths of Directories**
>> Word2vec:
  1. Training word2vec : C:\\Users\\bhavy\\OneDrive\\nlp\\data\\aclImdb\\train
  2. Loading word embedding for RNN : C:\\Users\\bhavy\\OneDrive\\nlp\\data\\aclImdb\\train\\word_vectors_word2vec.txt
  3. Testing RNN : C:\\Users\\bhavy\\OneDrive\\nlp\\data\\aclImdb\\test
>>FastText:
  1. Training word2vec : C:\\Users\\bhavy\\OneDrive\\nlp\\data\\aclImdb\\train
  2. Loading word embedding for RNN : C:\\Users\\bhavy\\OneDrive\\nlp\\data\\aclImdb\\train\\word_vectors_fastText.txt
  3. Testing RNN : C:\\Users\\bhavy\\OneDrive\\nlp\\data\\aclImdb\\test


**RNN model output using fastext model**
    Epoch 1/10: 100%|██████████████████████████████████████████████████████████████████████████████| 782/782 [03:49<00:00,  3.41batch/s]
    Training Loss: 0.6936
    Epoch 2/10: 100%|██████████████████████████████████████████████████████████████████████████████| 782/782 [03:50<00:00,  3.39batch/s]
    Training Loss: 0.6922
    Epoch 3/10: 100%|██████████████████████████████████████████████████████████████████████████████| 782/782 [03:04<00:00,  4.23batch/s]
    Training Loss: 0.6883
    Epoch 4/10: 100%|██████████████████████████████████████████████████████████████████████████████| 782/782 [02:00<00:00,  6.50batch/s]
    Training Loss: 0.6792
    Epoch 5/10: 100%|██████████████████████████████████████████████████████████████████████████████| 782/782 [02:00<00:00,  6.49batch/s]
    Training Loss: 0.6602
    Epoch 6/10: 100%|██████████████████████████████████████████████████████████████████████████████| 782/782 [02:00<00:00,  6.46batch/s]
    Training Loss: 0.6278
    Epoch 7/10: 100%|██████████████████████████████████████████████████████████████████████████████| 782/782 [02:01<00:00,  6.41batch/s]
    Training Loss: 0.5855
    Epoch 8/10: 100%|██████████████████████████████████████████████████████████████████████████████| 782/782 [02:00<00:00,  6.48batch/s]
    Training Loss: 0.5417
    Epoch 9/10: 100%|██████████████████████████████████████████████████████████████████████████████| 782/782 [02:01<00:00,  6.41batch/s]
    Training Loss: 0.5018
    Epoch 10/10: 100%|█████████████████████████████████████████████████████████████████████████████| 782/782 [01:59<00:00,  6.52batch/s]
    Training Loss: 0.4666
    Testing: 100%|█████████████████████████████████████████████████████████████████████████████████| 782/782 [00:10<00:00, 76.44batch/s]
    Test Accuracy: 0.5006
    Precision: 0.5010
    Recall: 0.2716
    F1-score: 0.3523
    
**RNN model output using word2vec using skipgram model with negative sampling**
    Epoch 1/10: 100%|█████████████████████████████████████████████████████████████████| 782/782 [00:34<00:00, 22.35batch/s]
    Training Loss: nan
    Epoch 2/10: 100%|█████████████████████████████████████████████████████████████████| 782/782 [00:35<00:00, 21.75batch/s]
    Training Loss: nan
    Epoch 3/10: 100%|█████████████████████████████████████████████████████████████████| 782/782 [00:38<00:00, 20.33batch/s]
    Training Loss: nan
    Epoch 4/10: 100%|█████████████████████████████████████████████████████████████████| 782/782 [00:46<00:00, 16.71batch/s]
    Training Loss: nan
    Epoch 5/10: 100%|█████████████████████████████████████████████████████████████████| 782/782 [00:51<00:00, 15.05batch/s]
    Training Loss: nan
    Epoch 6/10: 100%|█████████████████████████████████████████████████████████████████| 782/782 [00:53<00:00, 14.51batch/s]
    Training Loss: nan
    Epoch 7/10: 100%|█████████████████████████████████████████████████████████████████| 782/782 [00:46<00:00, 16.78batch/s]
    Training Loss: nan
    Epoch 8/10: 100%|█████████████████████████████████████████████████████████████████| 782/782 [00:52<00:00, 14.85batch/s]
    Training Loss: nan
    Epoch 9/10: 100%|█████████████████████████████████████████████████████████████████| 782/782 [00:51<00:00, 15.33batch/s]
    Training Loss: nan
    Epoch 10/10: 100%|████████████████████████████████████████████████████████████████| 782/782 [00:48<00:00, 15.99batch/s]
    Training Loss: nan
    Testing: 100%|███████████████████████████████████████████████████████████████████| 782/782 [00:07<00:00, 101.63batch/s]
    Test Accuracy: 0.5000
    Precision: 1.0000
    Recall: 0.0000
    F1-score: 0.0000

**Graph representation for Fasttext-RNN model**
  Training loss over epochs:
  ![image](https://github.com/Bhavyareddysadula/Readme/assets/126856102/52c418e2-512f-4b3b-83c9-0b480e4c155e)
  Evaluation metrics:
  ![image](https://github.com/Bhavyareddysadula/Readme/assets/126856102/bfe5e6b2-ccbb-4ffa-ae49-04af388271f1)



    
      
