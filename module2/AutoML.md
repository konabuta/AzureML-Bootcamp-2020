## 自動機械学習 Automated Machine Learning
Azure Machine Learning に含まれる自動機械学習 Automated Machine Learning は、**特徴量エンジニアリング & アルゴリズム選択 & パラメータ選択** を全自動で行います。現在は、**表形式データ (Tabular Data)** をサポートしています。

<img src="media/automl.gif"><br/>

自動機械学習で必要な設定は3つです。
- Dataset : 学習に必要なデータの準備
- Optimization Metric: 機械学習の種類、精度指標の指定
- Constrains : 試行するパイプライン数、最大実行時間の指定

<img src="https://docs.microsoft.com/ja-jp/azure/machine-learning/service/media/tutorial-auto-train-models/flow2.png" width=400>
<br/><br/>