# WAT

Musical instruments analysys

![confusion matrix](https://github.com/syzer/sentiment-instruments/blob/master/data/confusion_matrix.png)

- reviewer ID ​- IDof the reviewer, e.g.A​ 2SUAM1J3GNN3B
- asin​ - ID of the product, e.g.​​0000013714
- reviewerName ​- name of the reviewer
- helpful ​- helpfulness rating ofthe review, e.g.2/3
- reviewText ​- text of the review
- overall​ - rating of the product
- summary​ - summary of the review
- unixReviewTime​ - time of the review(unixtime)
- reviewTime​ - time of the review(raw)

# About
Bag of words is very simple model, that trains fast.
Other approaches are listed in `Extensions` section

# Install
```bash
pip install -r requirements.txt
./install.sh
```

# Training of model
```bash
python train3.pyy
```

# Server to show results
```bash
python serve_model.pyy
```

# Test
Please start the server and then
```bash
./test.sh
```

# Extensions
These are next steps I would try(not necessary in presented order)
- [ ] Normalization/Data Resampling: 
    - to battle inbalance
    - Use Quantile transformer
    - use weigh
    - Initialize weights of model/ regularization l1

- LSTM
- LSTM + Attention
- Add Conv1D - for filtering out some `boring` words
- n-gram (tri-gram)
- Embedings
    - example use GLOVE word embeddings
    - should be faster than LSTM
- Last layer with:
    ```model.add(layers.Dense(1, activation=tf.nn.sigmoid))```
    Now is categorical /discreate... so output could be 3.5 Stars, so then we would cast it to 4 stars
