# DIP_A
AELGNet implentaion, based on the paper AELGNet: Attention-based Enhanced Local and Global Features Network formedicinal leaf and plant classification

Link: https://doi.org/10.1016/j.compbiomed.2024.109447

The model was trained and validated on the Indian Medicinal Leaves Dataset (https://www.kaggle.com/datasets/aryashah2k/indian-medicinal-leaves-dataset)

AELGNet.ipnyb is the latest and correctly running file for the implementation. Code is self contained and should work, as long as you have the dataset.
The first time you run it, you will have to also run the commented block of code that preprocceses the dataset with clahe. This ensures that the cpu doesnt bottleneck the gpu should
we train and apply clahe during training.


The paper seems to have implemented a different version of MBConv block than what is industry standard. I have implemented both, and the module name for paper_MBConv can be swapped
with the MBConv implementation below to train it on that. In general, higher accuracies using the standard MBConv Block were noticed.
