# WAT

Musical instruments analysys

![alt text](https://github.com/syzer/sentiment-instruments/blob/master/data/ConfusionMatrix.jpg)

- reviewer ID​-IDofthereviewer,e.g.A​ 2SUAM1J3GNN3B
- asin​ -IDoftheproduct,e.g.​​0000013714
- reviewerName ​-nameofthereviewer
- helpful ​-helpfulnessratingofthereview,e.g.2/3
- reviewText ​-textofthereview
- overall​ -ratingoftheproduct
- summary​ -summaryofthereview
- unixReviewTime​ -timeofthereview(unixtime)
- reviewTime​ -timeofthereview(raw)

# Install
```bash
pip install -r requirements.txt
```


# How
```bash
python train3.pyy
```

server

```bash
python serve_model.pyy
```

# Test
```bash
curl "http://localhost:5000?text=good trumpet"
```
