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

鲜味肽(Umami)
Umami预测使用UmamiCNN模型
使用方法：建模数据集包括训练集和测试集，其中训练集共491个肽段，鲜味肽数量为246；训练集共123个肽段，鲜味肽数量为61；基于蛋白质语言模型ESM-2和卷积神经网路模型（CNN），在训练集进行十倍交叉验证，之后在测试集进行测试。十倍交叉验证中，UmamiCNN平均准确率为0.89，最佳模型的准确率为0.98；在独立测试集中，准确率为0.85，其中对鲜味肽预测准确为0.89，非鲜味肽预测准确率为0.82. 有关详细的建模方法在AHTPeptideFusion参考论文中可以找到。
参考文献：Pan F, Liu D, Tuersuntuoheti T, et al. Mining anti-hypertensive peptides in animal food through deep learning: a case study of gastrointestinal digestive products of royal jelly. Food Science of Animal Products, 2024, 2(1): 9240053. https://doi.org/10.26599/FSAP.2024.9240053

体外抗氧化模型（DPPH\ABTS\FRAP\ORCA）
ABTS：训练集432：活性肽225和非活性肽207，测试集108：活性肽48和非活性肽60。
DPPH：训练集286：活性肽170和非活性肽116，测试集71：活性肽34和非活性肽37。
FRAP：训练集457：活性肽255和非活性肽202，测试集114：活性肽45和非活性肽69。
ORCA：训练集408：活性肽204和非活性肽204，测试集92：活性肽47和非活性肽45。
使用方法：基于蛋白质语言模型ESM-2和卷积神经网路模型（CNN），在训练集进行十倍交叉验证，之后在测试集进行测试。十倍交叉验证中，ABTS\DPPH\FRAP\ORCA平均准确率分别为0.84、0.92、0.87和0.90，最佳模型的准确率分别为0.98、0.97、0.98和0.98；在独立测试集中，分别准确率为0.84、0.87、0.89和0.91，其中对活性肽预测准确分别为0.8、0.88、0.92和0.91，非活性肽预测准确率分别为0.88、0.87、0.88和0.91。
有关详细的建模方法在AHTPeptideFusion参考论文中可以找到。
参考文献：Pan F, Liu D, Tuersuntuoheti T, et al. Mining anti-hypertensive peptides in animal food through deep learning: a case study of gastrointestinal digestive products of royal jelly. Food Science of Animal Products, 2024, 2(1): 9240053. https://doi.org/10.26599/FSAP.2024.9240053

过敏原性肽(pLM4Alg)
过敏原性肽预测使用pLM4Alg模型
参考文献：Zhenjiao Du, Yixiang Xu, Changqi Liu, and Yonghui Li*. pLM4Alg: Protein Language Model-Based Predictors for Allergenic Proteins and Peptides, J. Agric. Food Chem. 2024, 72, 1, 752–760, https://doi.org/10.1021/acs.jafc.3c07143

抗癌肽(ACP)
ACP预测使用TriNet模型
参考文献：Jiyun Han,1 Shizhuo Zhang,1 and Juntao Liu1,2,3,*. Protocol for predicting peptides with anticancer and antimicrobial properties by a tri-fusion neural network, Star Protocols, DOI: 10.1016/j.xpro.2023.102541

抗炎肽(AIP)
AIP预测使用PREDAIP模型
参考资料：PREDAIP: Computational Prediction and Analysis for Anti-inflammatory Peptide via a Hybrid Feature Selection Technique

毒性肽（toxin）
toxin预测使用toxinpred3模型
参考资料：ToxinPred 3.0: An improved method for predicting the toxicity of peptides

抗菌肽（AMP）
革兰氏阴性菌和革兰氏阳性菌AMP预测使用CalcAMP模型
参考资料：Bournez C, Riool M, de Boer L, Cordfunke RA, de Best L, van Leeuwen R, Drijfhout JW, Zaat SAJ, van Westen GJP. CalcAMP: A New Machine Learning Model for the Accurate Prediction of Antimicrobial Activity of Peptides. Antibiotics (Basel). 2023 Apr 7;12(4):725. doi: 10.3390/antibiotics12040725.

苦味肽（Bitter）
Bitter预测使用Bitter-RF模型
参考资料：Zhang YF, Wang YH, Gu ZF, Pan XR, Li J, Ding H, Zhang Y, Deng KJ. Bitter-RF: A random forest machine model for recognizing bitter peptides. Front Med (Lausanne). 2023 Jan 26;10:1052923. doi: 10.3389/fmed.2023.1052923.
