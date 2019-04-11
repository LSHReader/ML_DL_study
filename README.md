# Studying Concept

### AUC(AUROC), AUPR
##### 1.[AUC 설명](https://tykimos.github.io/2017/05/22/Evaluation_Talk/)  
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
