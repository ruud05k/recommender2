See analysis3.ipynb for Jupyter notebook.

Summary of findings:
Various models were explored for predicting book ratings (explicit user feedback). These include k-nearest neighbors (KNNBasic), matrix factorization (SVD and SVDpp), item-based collaborative filtering (SlopeOne), and a two-tower neural network. SVD and the two-tower neural network performed best for this dataset.

In contrast to SVD, the two-tower neural network can incorporate additional contextual features, such as user age and location. This is especially beneficial for users with limited interaction history, thus partially resolving cold start issues. Further, the neural network architecture is scalable and can easily be parallelized across multiple computational nodes, unlike SVD with its sequential nature.

In addition, implicit user feedback was seperately modeled. In e-commerce environments, implicit user feedback (e.g. clicks) is much more abundant. On the hold-out test set, good performance was achieved on the implicit feedback dataset with an ROC-AUC and PR-AUC of 0.94 and 0.95, respectively.

With these models, a ranked list of items could be produced for a certain user, whereby the ranking is determined based on the predicted user rating and / or predicted click probability. 

