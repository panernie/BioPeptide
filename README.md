# BioPeptide
Prediction models of multiple active peptides

降血压肽
ACE抑制肽预测使用AHTPeptideFusion模型
使用方法：基于蛋白质语言模型和深度学习的分段融合方法建立的预测模型——AHTPeptideFusion。在12种机器学习(ML)算法中，Transformer优于其他11种模型，在预测短肽和中肽方面表现最佳。在外部数据集中，Transformer和随机森林(RF)融合的AHTPeptideFusion在预测长度为2 ~ 15个氨基酸残基和不同活性分布的ACE-I抑制肽方面表现出优异的性能(准确率> 0.9)。
参考文献：Pan F, Liu D, Tuersuntuoheti T, et al. Mining anti-hypertensive peptides in animal food through deep learning: a case study of gastrointestinal digestive products of royal jelly. Food Science of Animal Products, 2024, 2(1): 9240053. https://doi.org/10.26599/FSAP.2024.9240053

糖苷酶抑制肽
LBSPP预测使用LBSPP模型
使用方法：从文献中收集208个糖苷酶抑制肽数据，将糖苷酶抑制活性IC50阈值定义为10mM，当IC50小于10mM认为有抑制活性，当IC50大于10mM认为有低抑制活性或者无抑制活性；按照8:2划分为训练集和测试集，其中训练集包括69个高抑制活性肽段和96个低抑制或者无抑制活性肽段；测试集包括17个高抑制活性肽段和25个低抑制或者无抑制活性肽段。LBSPP模型建立是基于蛋白质语言模型ESM-2和卷积神经网路模型（CNN），在训练集进行五倍交叉验证，之后在测试集进行测试。在测试集中，LBSPP的准确率为0.71，其中识别高抑制活性肽段的precision、recall和f1分别为0.72,0.84和0.78，而识别低抑制或者无抑制活性肽段的precision、recall和f1分别为0.69,0.53和0.6，该模型准确率显著优于分子对接。有关详细的建模方法在AHTPeptideFusion参考论文中可以找到。
参考文献：Pan F, Liu D, Tuersuntuoheti T, et al. Mining anti-hypertensive peptides in animal food through deep learning: a case study of gastrointestinal digestive products of royal jelly. Food Science of Animal Products, 2024, 2(1): 9240053. https://doi.org/10.26599/FSAP.2024.9240053
![Uploading image.png…]()
LBSPP在训练集和测试集的模型性能表现

![Uploading image.png…]()
基于分子对接识别高活性和低抑制或者无抑制活性肽段的性能表现
