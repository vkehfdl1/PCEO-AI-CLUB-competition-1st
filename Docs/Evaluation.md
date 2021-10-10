이번 대회에의 평가 방식으로 [MAE](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_error.html)를 사용합니다. 실제 학생의 시험 점수와 AI로 예측한 시험 점수간의 오차를 계산하는 것입니다. 
아래 코드를 사용하여 계산할 수 있습니다.
```
from sklearn.metrics import mean_absolute_error
mean_absolute_error(y_pred, y_true)
```
