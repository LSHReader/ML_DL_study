# Studying ML/DL  

### AUC(AUROC), AUPR
##### 1. [AUC 설명](https://tykimos.github.io/2017/05/22/Evaluation_Talk/)  
AUC = Area under the curve
sensitivity(recall) = 실제 정상값들 중 정상으로 분류한 비율  
specificity = 실제 비정상값들 중 비정상으로 분류한 비율  
sensitivity 클수록 좋다. specificity 클수록 좋다.  
클래스를 구분하는 임계값(threshold)에 따라 sensitivity/(1-specificity) 값이 달라진다.  

##### 2. [AUPR 설명](http://www.chioka.in/differences-between-roc-auc-and-pr-auc/)  
PR curve = Precision Recall Curve
AURR = Area under PR Curve  
언제 PR curve를 쓰는가? = positive sample에 비하여 negative sample이 많은 경우(imbalance data)  
Precision = 정상이라고 답한 것들 중에 실제 정상인 비율  
Recall(sensitivity) = 실제 정상인 것들 중에 정상이라고 답한 것들의 비율  
클래스를 구분하는 임계값(threshold)에 따라 precision/recall 값이 달라진다.(이 값 자체가 커야 좋은지? 에 대한 이유는 잘 모르겠음, 더 생각해보기)  
AUPR이 1에 가까운 것이 좋다.  

### Anomaly Detection, Novelty Detection  
##### 1. Anomaly Detection  == outlier detection 인지..?(공부 더 필요)  
anomaly detection = detecting abnormal or unusual observations  
outlier detection = unsupervised anomaly detection  -> outliers/anomalies 가 저밀도 지역에 존재한다고 가정하므로, dense cluster를 형성할 수 없다.  
novelty detection = semi-supervised anomaly detection  -> 정상 데이터로 간주되는 training data의 저밀도 지역 내에서, novelties/anomalies는 dense cluster을 형성할 수 있다.  
##### 2. Novelty Detection  
clean한 데이터셋(outlier가 없는)에 새로운 데이터가 들어왔을 때, 기존 clean data set이 형성하는 분포 내에 들어오면 이상치가 아니고, 분포 밖에 들어오면 이상치라고 취급한다.  
[scikit-learn](https://scikit-learn.org/stable/modules/outlier_detection.html): The training data is not polluted by outliers and we are interested in detecting whether a __new__ observation is an outlier. In this context an outlier is also called a novelty.
##### 3. Outlier Detection
outlier가 포함된 데이터셋에서 진행.  
대다수의 같은 분포를 형성하고 있는 데이터셋에서 동떨어져 있는 데이터를 outlier로 취급.  
[scikit-learn](https://scikit-learn.org/stable/modules/outlier_detection.html): The training data contains outliers which are defined as observations that are far from the others. Outlier detection estimators thus try to fit the regions where the training data is the most concentrated, ignoring the deviant observations.   
