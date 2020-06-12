---
layout: post
title: Bike Sharing - Submit Record
date: 2020-06-12
description: Kaggle's Bike Sharing - Submit Record
thumbnail: work1.jpg
categories: DataMining

# Information for the author block
author : Loui
---


2020-05-14
- 첫날 시도, feature 몇개 지움

2020-05-15
- windspeed value 0 인거 제대로 처리하고, count에 log취해서 예측한뒤 다시 exp해줌.
> xgboost : 3.08736 ?? 뭔가 잘못 됐는데? 아 submit값에 exp를 안해줬다. 

 제대로 처리해줌
> xgboost : 0.42295
> lightgbm : 0.41943 ==> 438/3242 == 0.13
> RandomForest : 0.45994

2020-05-16
- one hot encoding 했는데, valid score는 더 안 좋아 진 것 같다. 
> RandomForest : 0.67865
- 결과가 상당히 안 좋다. one hot encoding 안해야 겠다.
>> 위에 것 모르고 weather를 넣고 workingday를 뺀 데이터 프레임이다. 그런데 수정해도 그렇게 좋은 결과는 안 나올것 같다. 그래도 3개다 해보겠다.
> lightGBM : 0.45753
> RandomForest : 0.45983
> XGBoost : 0.45690
>> 일괄적으로 구리게 나왔다. one hot encoding 안 하는게 확실히 더 좋은듯 하다.

- one hot 후에 correlation 보니까 temp랑 계절이랑 꽤 높게 나왔다. 그래서 season을 다빼고 해보았다.
> XGBoost : 0.45919
> LightGBM : 0.45941
> RandomForest : 0.48220

>> 흠 역시 별로다. 어떻게 해야 더 Score 내릴 수 있지?
>> GridSearch 해봐야되나?

- LightGBM Grid하고 있는데 iteration 10000번 돌아야된다.. 너무오래걸려서 인적성 공부하고 있어야겠다..
> 만번 넘어가서 줄였다.
> #Best parameters: {'early_stopping_rounds': 20, 'learning_rate': 0.1, 'max_depth': 34, 'n_estimators': 340, 'num_leaves': 73} 이렇게 나왔다.
>> lightGBM : 0.43854. 

- 아 일단 categorical feature 처리를 안해줬다.
해준게 lgb_score : 0.17393705465388506
> lightGBM : 0.42856
확실히 categoricla feature를 처리해줘야한다.

- 와 도대체 15일에는 어케저게 나온거누? 아 저거는 xgb_boost로 windspeed예측한거다. 그걸로 해봐야겠다.
> 이렇게 해준게 lgb_score : 0.17393705465388506
와 xx 어케 똑같누? lightgbm이랑 xgboost랑 성능 진짜 비슷한가 본데?
> ligthGBM : 0.42856
>> 이야 똑같네.. 그럼 wind speed를 예측하는데 lgb나 xgb나 똑같다는 소리다.
>>> 이거 내가 잘못한거같은데? ㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋ
>>> 내가 xgb모델을 lgb모델 예측할때 써버렷음 ㅎㅎ.. 다시하자
> 이거 valid score : 0.17464327095206544
>> lightGBM : 0.42702
> lightGBM으로 예측한 게 더 좋네.

- 와그러면 진짜 05 15 에 score 4.1은 어케 나온 거고?
> 오늘은 여기까지만 하자

2020-05-17
-오늘할거는 wind speed 예측을 train set으로만 하는 거를 일단 할거다.
> lgb가 더 예측 좋게 했으니까. lightGBM으로 예측해 보자.
> RandomForest : 0.45923 ( valid : 0.13312854204587843)
> LightGBM : 0.42652 (valid : 0.1747456168077491)
> XGBoost :  0.42256 (valid : 0.29858466091399916)

>>흠 진짜 15일의 4.1은 어케나왔지?ㅋㅋㅋㅋㅋㅋㅋㅋㅋ
>> 여튼 train set으로만 wind 예측하는 게 더 좋은 결과를 낸다.

- 다음은 humidity를 살려보자.
> XGBoost :  0.42103 (valid : 0.2890292937260758)
> LightGBM : 0.42598 (valid : 0.1430996449478506)
> RandomForest :  0.44876 (valid : 0.1225284909994309)
>> 오늘은 여기까지만 하자. 

2020-05-19
- 복잡하니까 오늘 한 거를 모두 적어본다
- atemp, day, casual, registered 지웠고, holiday 살렸음.
- wind ==0 은 lgb로 예측했고, count는 outlier제거함 3 std 이상인거 제거함.
- count 예측은 log값으로 해주었음.
> XGB : 0.42389 (valid : 0.28283237043020293)
> LGB :  0.42250 (valid : 0.13986006236976856)
> RF : 0.44286 (valid : 0.11991216644158816)
>> 와 4.1이 아직도 안나오네

- xgb로 wind 예측한걸로 해보았다.
> XGB : 0.42004(valid : 0.28328653334621345)
> LGB :  0.42456(valid : 0.14006168374986241)
> RF : 0.44713(valid : 0.11982588596672973)
>> 흠 XGBoost 가 0.42 까지 내려갔네? 다른거는 올랐는데.

- 보니까 weather는 category로 안바꿔도 될 거 같음. 1 올라갈때 마다 날씨가 나빠지니까.
- weather는 카테고리로 안바꾸고 함 해보겠음. XGBoost는 어차피 카테고리 안되니까, LGB랑 RF만 해봄.
- 심지어 weather랑 holiday도 one hot 된거라서 안해도됨.

> XGB로 wind 처리한 거 먼저
> LGB :  0.42186(valid : 0.1366881490007631
> RF : 0.44707(valid : 0.12085121824015463

> LGB로 wind 처리한 거
> LGB :  0.42250 (valid : 0.13896253501948003
> RF :  0.44286 (valid : 0.12084603181103722

- LGB로 4.1 받은거 확인해봤는데 valid가 0.28임. 근데 요근래 valid는 0.13 인거보니까 요새 train에 너무 overfit되는 거 같음.
- Gridsearch한거 말고 기본값으로 해봐야겠음.
> 이거는 카테고리 안바꾼거에 LGB파라미터를 default로 주고 round==100준거. 즉 LGB값만 확인
> LGB : 0.41242 (valid : 0.26242399512337594) 일단 예상대로 valid는 0.26이 나옴.
>> 아 kaggle일 안하네? 왜캐 오래걸려 예측이!!!!!!!!!!!!!!
>> 그렇다.. overfit이었다... valid가 너무 낮으면 안좋네
>>> 이거 순위 365/3242 11.2%. 와 10% 밑으로 어케 내리누!


- 이때까지 보니까 RF가 결과적으로 XGBoost랑 LgihtGBM 못따라간다.

[2020-05-21]
오늘은 유튜브 todaycode를 참고하였다.
todaycode에서는 모든 컬럼을 다 살리더라... 그래서 나도 그렇게 해보았다.

- 일단 dayofweek 를 추가하였다. 그리고 log 도 np.log1p로 바꾸었다.

- 먼저 xgb로 wind pred한것이다.
이거 잘못했따. xgb로 예측하고 lgb로 테스트했다.
> XGB : 0.40990(valid : 0.24657067064627095
> LGB :  0.40809(valid : 0.22745710457204094
> RF : 0.43908 (valid : 0.1038587481612548

- 제대로 한것이다.
> XGB : 0.40990(valid : 0.24657067064627095
> LGB :  0.40793(valid : 0.24657067064627095) <== 307/3242 , 상위 0.09, 상위 9%
> RF : 0.43803(valid : 0.1034414633765208


- 다음은 lgb로 wind pred한것이다.
> XGB : 0.41049(valid : 0.24657067064627095
> LGB :  0.41125(valid : 0.22573125442557038
> RF : 0.43799(valid : 0.10332807018474177

>>와 모든 컬럼 넣는게 훨씬 좋네...  드디어 상위 10%를 뚫었다.

- 다음은 windspeed를 그냥 버려버리는 것이다.  windspeed 버리고, 나머지 컬럼 다살리고 dayofweek 넣고 돌려보았다.
> XGB : 0.41501(valid : 0.24705335192005412
> LGB :  0.41027(valid : 0.23530627736535958
> RF : 0.43970(valid : 0.10320715019300583
>> 이거는 LGB하고 RF에서 categorical feature 처리 안해준 것이다. 처리해주고 다시 해보겠다.

> LGB :  0.41514(valid : 0.22931192113551588
> RF : 0.43267(valid : 0.10298417871435152

>>나는 windspeed 예측한게 좀 더 좋게 나온다.

- 이 다음 거는 windspeed 지우고 month도 지운것이다. categorical 처리도 해주었다.
> XGB : 0.38917(valid : 0.2558400247388624
> LGB :  0.38522(valid : 0.23886619975961224 <== 135/3242 , 상위 0.04, 상위 4%
> RF : 0.39853(valid : 0.10824603962341504

>> ??????????? 와 이거 뭐냐... month지우니까 이렇게 오른다고? 와 얼척이 없네 ㄷㄷ month가 그렇게 안좋은 feature였다니.. 전혀 예상 못했다.

- 그럼 month지우고 wind는 예측해서 해보자.
> xgb로 wind 예측 먼저

> XGB : 0.40990(valid : 0.24657)
> LGB : 0.40793  (valid : 0.22693550799257511 )
> RF : 0.43492 (valid : 0.1031020934243328)

> 그다음 LGB로 wind 예측 한거

> XGB : 0.41049 (valid : 0.2558400247388624) 
> LGB :  0.41125 (valid : 0.23886619975961224)
> RF :  0.43832 (valid : 0.10824603962341504) 

>> 견적 보니까 wind도 그냥 지워버리는 게 더 좋다. 
근데 나도 이건 생각을 했었던 건데, 주어진값으로 wind 예측을 하면 featrue들 간에 multilinearity가 더 높아져서 안 좋을 것 같았다.
즉, association 으로 빈 값을 예측하는 것은 정말 좋지 않다는 결과다. 그러므로 label값을 이용하는 것이 맞다고 생각한다.

와 그리고 month 지웠다고 오르는 건 어떻게 설명이 안되는 데?

- 마지막으로 month하고 wind그리고 mulitlinearity 가지고 있던 atemp를 지워보자.

> XGB : 0.39220 (valid : 0.2559842230814161)
> LGB :  0.38577 (valid : 0.2401462285908264)
> RF : 0.40058 (valid : 0.10760227645678314)

>> atemp는 있어야 하는게 더 좋다. 와 다중공선성도 무시하는 결관데? 이건 진짜 통계학적으로 의미를 찾아 볼수가 없는... 그런 결과다.
- 오늘은 여기까지 하자. 그래도 상위 4%로 올라왔다!


[2020-05-22 금요일]
오늘은 미국의 공휴일을 체크해서 count값을 반으로 줄여주자.
그리고 count대신 registered와 casual을 각각 예측한 후 합쳐주는 방식을 취하자.

- 이거는 holiday 처리 안한거
> XGB : 0.39845 (valid : 0.30315)
> LGB :  0.39456 (valid : 0.28258 )
> RF : 0.39771 (valid : 0.17847 )

- 이거는 처리한거
> XGB : 0.39254 (valid : 0.30315)
> LGB :  0.38822 (valid : 0.28258 ) <= 154/3242, 0.04, 상위 4%
> RF : 0.39771 (valid : 0.17847 )

>> 그냥 month하고 wind 지우고 count로 예측한 게 더 좋다.
>> 그리고 holiday 처리한게 더 좋다.

- holiday 처리한 거에 count로 한거 해보자.

> XGB : 0.38768 (valid : 0.25970) 
> LGB :  0.38548 (valid : 0.24253) <= 138/3242, 0.04, 상위 4%
> RF : 0.38768 (valid : 0.11037 )

>> 흠 holiday 처리안한 21일 것이 더 좋다.

- 오늘은 여기까지 하자.

XGBRegressor(base_score=0.5, booster='gbtree', colsample_bylevel=1,
             colsample_bynode=1, colsample_bytree=1, gamma=0,
             importance_type='gain', learning_rate=0.1, max_delta_step=0,
             max_depth=5, min_child_weight=1, missing=None, n_estimators=100,
             n_jobs=1, nthread=None, objective='reg:linear', random_state=0,
             reg_alpha=0, reg_lambda=1, scale_pos_weight=1, seed=None,
             silent=None, subsample=1, verbosity=1)
LGBMRegressor(boosting_type='gbdt', class_weight=None, colsample_bytree=1.0,
              importance_type='split', learning_rate=0.1, max_depth=-1,
              min_child_samples=20, min_child_weight=0.001, min_split_gain=0.0,
              n_estimators=100, n_jobs=-1, num_leaves=31, objective=None,
              random_state=None, reg_alpha=0.0, reg_lambda=0.0, silent=True,
              subsample=1.0, subsample_for_bin=200000, subsample_freq=0)
RandomForestRegressor(bootstrap=True, ccp_alpha=0.0, criterion='mse',
                      max_depth=None, max_features='auto', max_leaf_nodes=None,
                      max_samples=None, min_impurity_decrease=0.0,
                      min_impurity_split=None, min_samples_leaf=1,
                      min_samples_split=2, min_weight_fraction_leaf=0.0,
                      n_estimators=100, n_jobs=None, oob_score=False,
                      random_state=None, verbose=0, warm_start=False)

[2020-06-12 금요일]
- log1p로 count처리해주고 예측 후 expm1으로 원상복귀한 것.

> XGB : 0.38881: (valid : 0.26521 
> LGB : 0.38619 (valid : 0.24864 <= 143/3242, 0.04, 상위 4%
> RF : 0.40118 (valid : 0.12228 )
