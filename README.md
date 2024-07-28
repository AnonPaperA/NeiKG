
## Introduction
NeiKG: Knowledge Graph-driven Neighbor Selection and Aggregation for Long-tail Recommendation

## Environment Requirement
```
The code has been tested running under Python 3.7.10. The required packages are as follows:

torch == 1.8.0
numpy == 1.23.5
pandas == 1.5.3
scipy == 1.10.1
tqdm == 4.65.0
scikit-learn == 1.2.2
```

## NeiKG operation steps
1. run doCooccur.py to generate co-occurrence neighbors
```
python doCooccur.py
```
2. run selector.py to generate long-tail neighbors
```
python selector.py
```
3. start NeiKG
```
python main_NeiKG.py
```


## Datasets
We provided three datasets to validate NeiKG: Last-FM, MovieLens-1M, and Amazon-book.

|                | Last-FM |MovieLens-1M| Amazon-book |
| :------------: | :-----: |  :-----:   |:-----:   |
|    n_users     |  23566  |    6040    | 70679 |
|    n_items     |  48123  |    3655    |24915|
| n_interactions | 3034796 |   997579   |847733|
|   n_entities   | 58266  |   398505   | 88572|
|  n_relations   |    9    |     57     | 39|
|   n_triples    | 464567  |   3396595  |2557746|

We mapped items of three datasets to Freebase entities to construct KG.
The following table shows the KG information of three datasets:

| Knowledge Graph |   Freebase(Last-FM)   |  Freebase(MovieLens-1M)  | Freebase(Amazon-book)
|:---------------:|          :-----------:         |     :-------:     |:-------:     |
|   #entities    |              58266            |       398505      |88572|
|   #relations   |                 9              |         57        |39|
|    #triples    |              464567            |       3396595     |2557746|

