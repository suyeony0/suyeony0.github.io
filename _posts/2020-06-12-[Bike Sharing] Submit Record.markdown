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
- ù�� �õ�, feature � ����

2020-05-15
- windspeed value 0 �ΰ� ����� ó���ϰ�, count�� log���ؼ� �����ѵ� �ٽ� exp����.
> xgboost : 3.08736 ?? ���� �߸� �ƴµ�? �� submit���� exp�� �������. 

 ����� ó������
> xgboost : 0.42295
> lightgbm : 0.41943 ==> 438/3242 == 0.13
> RandomForest : 0.45994

2020-05-16
- one hot encoding �ߴµ�, valid score�� �� �� ���� �� �� ����. 
> RandomForest : 0.67865
- ����� ����� �� ����. one hot encoding ���ؾ� �ڴ�.
>> ���� �� �𸣰� weather�� �ְ� workingday�� �� ������ �������̴�. �׷��� �����ص� �׷��� ���� ����� �� ���ð� ����. �׷��� 3���� �غ��ڴ�.
> lightGBM : 0.45753
> RandomForest : 0.45983
> XGBoost : 0.45690
>> �ϰ������� ������ ���Դ�. one hot encoding �� �ϴ°� Ȯ���� �� ������ �ϴ�.

- one hot �Ŀ� correlation ���ϱ� temp�� �����̶� �� ���� ���Դ�. �׷��� season�� �ٻ��� �غ��Ҵ�.
> XGBoost : 0.45919
> LightGBM : 0.45941
> RandomForest : 0.48220

>> �� ���� ���δ�. ��� �ؾ� �� Score ���� �� ����?
>> GridSearch �غ��ߵǳ�?

- LightGBM Grid�ϰ� �ִµ� iteration 10000�� ���ƾߵȴ�.. �ʹ������ɷ��� ������ �����ϰ� �־�߰ڴ�..
> ���� �Ѿ�� �ٿ���.
> #Best parameters: {'early_stopping_rounds': 20, 'learning_rate': 0.1, 'max_depth': 34, 'n_estimators': 340, 'num_leaves': 73} �̷��� ���Դ�.
>> lightGBM : 0.43854. 

- �� �ϴ� categorical feature ó���� �������.
���ذ� lgb_score : 0.17393705465388506
> lightGBM : 0.42856
Ȯ���� categoricla feature�� ó��������Ѵ�.

- �� ����ü 15�Ͽ��� �������� ���°Ŵ�? �� ���Ŵ� xgb_boost�� windspeed�����ѰŴ�. �װɷ� �غ��߰ڴ�.
> �̷��� ���ذ� lgb_score : 0.17393705465388506
�� xx ���� �Ȱ���? lightgbm�̶� xgboost�� ���� ��¥ ����Ѱ� ����?
> ligthGBM : 0.42856
>> �̾� �Ȱ���.. �׷� wind speed�� �����ϴµ� lgb�� xgb�� �Ȱ��ٴ� �Ҹ���.
>>> �̰� ���� �߸��ѰŰ�����? ������������������������
>>> ���� xgb���� lgb�� �����Ҷ� ������� ����.. �ٽ�����
> �̰� valid score : 0.17464327095206544
>> lightGBM : 0.42702
> lightGBM���� ������ �� �� ����.

- �ͱ׷��� ��¥ 05 15 �� score 4.1�� ���� ���� �Ű�?
> ������ ��������� ����

2020-05-17
-�����ҰŴ� wind speed ������ train set���θ� �ϴ� �Ÿ� �ϴ� �ҰŴ�.
> lgb�� �� ���� ���� �����ϱ�. lightGBM���� ������ ����.
> RandomForest : 0.45923 ( valid : 0.13312854204587843)
> LightGBM : 0.42652 (valid : 0.1747456168077491)
> XGBoost :  0.42256 (valid : 0.29858466091399916)

>>�� ��¥ 15���� 4.1�� ���ɳ�����?������������������
>> ��ư train set���θ� wind �����ϴ� �� �� ���� ����� ����.

- ������ humidity�� �������.
> XGBoost :  0.42103 (valid : 0.2890292937260758)
> LightGBM : 0.42598 (valid : 0.1430996449478506)
> RandomForest :  0.44876 (valid : 0.1225284909994309)
>> ������ ��������� ����. 

2020-05-19
- �����ϴϱ� ���� �� �Ÿ� ��� �����
- atemp, day, casual, registered ������, holiday �����.
- wind ==0 �� lgb�� �����߰�, count�� outlier������ 3 std �̻��ΰ� ������.
- count ������ log������ ���־���.
> XGB : 0.42389 (valid : 0.28283237043020293)
> LGB :  0.42250 (valid : 0.13986006236976856)
> RF : 0.44286 (valid : 0.11991216644158816)
>> �� 4.1�� ������ �ȳ�����

- xgb�� wind �����Ѱɷ� �غ��Ҵ�.
> XGB : 0.42004(valid : 0.28328653334621345)
> LGB :  0.42456(valid : 0.14006168374986241)
> RF : 0.44713(valid : 0.11982588596672973)
>> �� XGBoost �� 0.42 ���� ��������? �ٸ��Ŵ� �ö��µ�.

- ���ϱ� weather�� category�� �ȹٲ㵵 �� �� ����. 1 �ö󰥶� ���� ������ �������ϱ�.
- weather�� ī�װ��� �ȹٲٰ� �� �غ�����. XGBoost�� ������ ī�װ� �ȵǴϱ�, LGB�� RF�� �غ�.
- ������ weather�� holiday�� one hot �ȰŶ� ���ص���.

> XGB�� wind ó���� �� ����
> LGB :  0.42186(valid : 0.1366881490007631
> RF : 0.44707(valid : 0.12085121824015463

> LGB�� wind ó���� ��
> LGB :  0.42250 (valid : 0.13896253501948003
> RF :  0.44286 (valid : 0.12084603181103722

- LGB�� 4.1 ������ Ȯ���غôµ� valid�� 0.28��. �ٵ� ��ٷ� valid�� 0.13 �ΰź��ϱ� ��� train�� �ʹ� overfit�Ǵ� �� ����.
- Gridsearch�Ѱ� ���� �⺻������ �غ��߰���.
> �̰Ŵ� ī�װ� �ȹٲ۰ſ� LGB�Ķ���͸� default�� �ְ� round==100�ذ�. �� LGB���� Ȯ��
> LGB : 0.41242 (valid : 0.26242399512337594) �ϴ� ������ valid�� 0.26�� ����.
>> �� kaggle�� ���ϳ�? ��ĳ �����ɷ� ������!!!!!!!!!!!!!!
>> �׷���.. overfit�̾���... valid�� �ʹ� ������ ������
>>> �̰� ���� 365/3242 11.2%. �� 10% ������ ���� ������!


- �̶����� ���ϱ� RF�� ��������� XGBoost�� LgihtGBM �����󰣴�.

[2020-05-21]
������ ��Ʃ�� todaycode�� �����Ͽ���.
todaycode������ ��� �÷��� �� �츮����... �׷��� ���� �׷��� �غ��Ҵ�.

- �ϴ� dayofweek �� �߰��Ͽ���. �׸��� log �� np.log1p�� �ٲپ���.

- ���� xgb�� wind pred�Ѱ��̴�.
�̰� �߸��ߵ�. xgb�� �����ϰ� lgb�� �׽�Ʈ�ߴ�.
> XGB : 0.40990(valid : 0.24657067064627095
> LGB :  0.40809(valid : 0.22745710457204094
> RF : 0.43908 (valid : 0.1038587481612548

- ����� �Ѱ��̴�.
> XGB : 0.40990(valid : 0.24657067064627095
> LGB :  0.40793(valid : 0.24657067064627095) <== 307/3242 , ���� 0.09, ���� 9%
> RF : 0.43803(valid : 0.1034414633765208


- ������ lgb�� wind pred�Ѱ��̴�.
> XGB : 0.41049(valid : 0.24657067064627095
> LGB :  0.41125(valid : 0.22573125442557038
> RF : 0.43799(valid : 0.10332807018474177

>>�� ��� �÷� �ִ°� �ξ� ����...  ���� ���� 10%�� �վ���.

- ������ windspeed�� �׳� ���������� ���̴�.  windspeed ������, ������ �÷� �ٻ츮�� dayofweek �ְ� �������Ҵ�.
> XGB : 0.41501(valid : 0.24705335192005412
> LGB :  0.41027(valid : 0.23530627736535958
> RF : 0.43970(valid : 0.10320715019300583
>> �̰Ŵ� LGB�ϰ� RF���� categorical feature ó�� ������ ���̴�. ó�����ְ� �ٽ� �غ��ڴ�.

> LGB :  0.41514(valid : 0.22931192113551588
> RF : 0.43267(valid : 0.10298417871435152

>>���� windspeed �����Ѱ� �� �� ���� ���´�.

- �� ���� �Ŵ� windspeed ����� month�� ������̴�. categorical ó���� ���־���.
> XGB : 0.38917(valid : 0.2558400247388624
> LGB :  0.38522(valid : 0.23886619975961224 <== 135/3242 , ���� 0.04, ���� 4%
> RF : 0.39853(valid : 0.10824603962341504

>> ??????????? �� �̰� ����... month����ϱ� �̷��� �����ٰ�? �� ��ô�� ���� ���� month�� �׷��� ������ feature���ٴ�.. ���� ���� ���ߴ�.

- �׷� month����� wind�� �����ؼ� �غ���.
> xgb�� wind ���� ����

> XGB : 0.40990(valid : 0.24657)
> LGB : 0.40793  (valid : 0.22693550799257511 )
> RF : 0.43492 (valid : 0.1031020934243328)

> �״��� LGB�� wind ���� �Ѱ�

> XGB : 0.41049 (valid : 0.2558400247388624) 
> LGB :  0.41125 (valid : 0.23886619975961224)
> RF :  0.43832 (valid : 0.10824603962341504) 

>> ���� ���ϱ� wind�� �׳� ���������� �� �� ����. 
�ٵ� ���� �̰� ������ �߾��� �ǵ�, �־��������� wind ������ �ϸ� featrue�� ���� multilinearity�� �� �������� �� ���� �� ���Ҵ�.
��, association ���� �� ���� �����ϴ� ���� ���� ���� �ʴٴ� �����. �׷��Ƿ� label���� �̿��ϴ� ���� �´ٰ� �����Ѵ�.

�� �׸��� month �����ٰ� ������ �� ��� ������ �ȵǴ� ��?

- ���������� month�ϰ� wind�׸��� mulitlinearity ������ �ִ� atemp�� ��������.

> XGB : 0.39220 (valid : 0.2559842230814161)
> LGB :  0.38577 (valid : 0.2401462285908264)
> RF : 0.40058 (valid : 0.10760227645678314)

>> atemp�� �־�� �ϴ°� �� ����. �� ���߰������� �����ϴ� �����? �̰� ��¥ ����������� �ǹ̸� ã�� ������ ����... �׷� �����.
- ������ ������� ����. �׷��� ���� 4%�� �ö�Դ�!


[2020-05-22 �ݿ���]
������ �̱��� �������� üũ�ؼ� count���� ������ �ٿ�����.
�׸��� count��� registered�� casual�� ���� ������ �� �����ִ� ����� ������.

- �̰Ŵ� holiday ó�� ���Ѱ�
> XGB : 0.39845 (valid : 0.30315)
> LGB :  0.39456 (valid : 0.28258 )
> RF : 0.39771 (valid : 0.17847 )

- �̰Ŵ� ó���Ѱ�
> XGB : 0.39254 (valid : 0.30315)
> LGB :  0.38822 (valid : 0.28258 ) <= 154/3242, 0.04, ���� 4%
> RF : 0.39771 (valid : 0.17847 )

>> �׳� month�ϰ� wind ����� count�� ������ �� �� ����.
>> �׸��� holiday ó���Ѱ� �� ����.

- holiday ó���� �ſ� count�� �Ѱ� �غ���.

> XGB : 0.38768 (valid : 0.25970) 
> LGB :  0.38548 (valid : 0.24253) <= 138/3242, 0.04, ���� 4%
> RF : 0.38768 (valid : 0.11037 )

>> �� holiday ó������ 21�� ���� �� ����.

- ������ ������� ����.

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

[2020-06-12 �ݿ���]
- log1p�� countó�����ְ� ���� �� expm1���� ���󺹱��� ��.

> XGB : 0.38881: (valid : 0.26521 
> LGB : 0.38619 (valid : 0.24864 <= 143/3242, 0.04, ���� 4%
> RF : 0.40118 (valid : 0.12228 )
