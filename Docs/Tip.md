# [Tip] 시도해 볼 만한 것들

대회 Host 김동규입니다. 캐글에서의 대회가 아직 익숙하지 않아, 점수를 올리는 것에 어려움을 겪을 수 있는 분들을 위하여, 이번 대회에서 점수를 올리기 위해 시도해 볼 만한 것들을 정리하였습니다.

---
## 데이터 전처리
### 디테일한 EDA
먼저 데이터를 가장 잘 아는 것이 중요하겠죠. Pandas, matplotlib, seaborn 등을 이용하여 데이터의 그래프를 그려보고 이리저리 통계적인 분석과 접근을 할 수 있습니다.

### 새 Feature 만들기
EDA를 하며 얻은 insight나 창의적인 아이디어를 이용하여 새로운 feature를 만들 수 있습니다. 혹은, PCA나 Kmeans 등 다양한 통계적 기법을 사용해 새 feature를 만들어 볼 수 있습니다.

### Encoder 변경
categorical 변수들을 숫자로 바꾸는 것은 classical ML에서 상당히 중요한 부분입니다. Ordinal Encoder 대신 One-Hot Encoder 등 다양한 Encoder를 사용해 categorical 변수들을 새로운 방식으로 접근해 볼 수 있습니다.

### 새로운 train-validation 나누기
단순하게 랜덤으로 나누는 것이 아닌 다른 방식으로 나누어 볼 수 있습니다.

### 기존 feature 지우기
언제나 최후의 방법이지만, 경우에 따라서는 데이터를 줄이는 것이 도움이 될 수 있습니다.

---
## 모델링
### 새로운 모델 사용하기
언제까지 RandomForest만 사용할 수는 없죠. LGBM, Catboost, XGboost 등 다양하고 무거운 모델을 사용할 수 있습니다. 아예 DNN 네트워크를 직접 구성할 수도, Denoising AutoEncoder나 GAN 같은 굉장히 복잡하고 어려운 모델을 도전적으로 실험할 수도 있습니다. 혹은 LinearRegression 같은 단순한 모델을 사용하면 오히려 더 좋은 결과가 나올 수도 있습니다. 가능성은 무한합니다!

### Hyperparameter tuning
모델을 정했다면 그 모델의 극한까지의 성능을 도달하는 것이 필요합니다. 단순하게 숫자를 조금 바꾸는 것으로 시작하여 optuna와 같은 자동 튜닝 모델을 사용하고, 심지어는 AutoML을 사용할 수도 있습니다. 하지만 항상 overfitting은 주의해야 하는 점 기억하세요.

### Learning Rate Scheduler
Hyperparameter 중 Learning Rate는 모델이 훈련됨에 따라서 동적으로 조절하는 경우도 있습니다. cosine decay 등 수많은 방법이 소개되어 있는데요. 이것을 적용하는 것이 어쩌면 도움이 될 수도 있겠죠?

### 새로운 loss function
loss function을 꼭 주어진 평가 방법인 MAE를 사용하지 않아도 괜찮습니다. 다른 loss function을 사용하거나 심지어 직접 loss function을 만들어 볼 수도 있습니다.

---
## 기타
### Cross Validation
Overfitting을 방지하기 위해서 굉장히 중요한 기술입니다. Cross Validation의 중요성은 정말 높은데요, 반드시 높은 성능을 보장하는 기술은 아니지만, 모델의 안정적인 성능 만큼은 보장할 수 있습니다.

### Ensemble
앙상블은 tabular data 대회의 꽃과 같은 기술입니다. stacking, voting, boosting, blending 등등 수많은 앙상블 기법이 있고, submission 파일들과 새로운 모델들은 넘쳐납니다. 이것들을 하나만 활용하지 않고 앙상블을 이용해 하나로 합쳐서 더 높은 점수를 달성해보세요!

### Pseudo Labelling
훈련할 데이터를 더욱 늘릴 수 있을까요? 이 고민에서 시작된 것이 semi-supervised learning의 일종인 pseudo labelling입니다. test 데이터를 예측 후, 그것까지 훈련에 사용한다면 더욱 정확한 모델이 나올 수도 있습니다.

### Label smoothing
모델 훈련으로 나온 결과는 다시 건드리지 말라는 법은 없습니다. 이 기법을 통하여 너무 작거나 너무 큰, outlier들의 점수를 평균과 비슷하게 만들어서 크게 증가할 수 있는 오류를 줄여볼 수 있습니다.

위에서 언급한 기법들 이외에도 더욱 다양하고 창의적인 방법으로 리더보드 상단으로 점수를 올려볼 수 있습니다. 이 글이 '뭘 어떻게 해야 하지?'하는 여러분들에게 조그마한 답이 되었으면 좋겠네요.
마지막으로 중요한 것은, Code 탭에 자신의 Code를 공유하는 것 입니다. 처음부터 해당 탭에서 Code를 생성하고, 공유할 준비가 되면 Share에서 Public으로 바꾸고, Save Version을 클릭하여 공유해주세요!