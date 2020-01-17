# Azure Machine Learning Bootcamp

Azure Machine learning Bootcamp のサンプルコードです。

## Draft
- **Module 0 : 環境準備**
    - Azure Machine Learning ワークスペース作成
    - Notebook VM (Compute Instance) 作成
    - Training Cluster 作成

- **Module 1 : 機械学習概論 & Azure Machine Learning ご紹介**
    - 機械学習概論
    - Azure Machine Learning 概要

- **Module 2 : 自動機械学習 Automated ML ハンズオン**
    - データのダウンロード
        - データ : [nyc-taxi-sample-data.csv](https://quickstartsws9073123377.blob.core.windows.net/azureml-blobstore-0d1c4218-a5f9-418b-bf55-902b65277b85/quickstarts/nyc-taxi-data/nyc-taxi-sample-data.csv)
    - データセット登録
    - 自動機械学習 Automated Machine Learning
        - GUI
        - Python SDK
    - 結果の理解
    - Strech Goal
        - 与信管理モデル学習
            - データ : [hmeq_ja.csv](https://github.com/konabuta/Automated-ML-Workshop/blob/master/data/hmeq_ja.csv)
- **Module 3 : 機械学習モデルの解釈 ハンズオン**
    - Notebook VM の起動
    - Python SDK による自動機械学習
    - モデルの解釈
    - Strech Goal
        - [scikit-learn モデルの解釈](https://github.com/solliancenet/azure-machine-learning-quickstarts/blob/master/aml-python-sdk/starter-artifacts/nbvm-notebooks/06-aml-interpretability/solution-interpretability-with-AML.ipynb)


- **Module 4 : モデルのデプロイと運用 ハンズオン**
    - Pytorch Estimator によるモデル開発
    - 画像認識モデルのデプロイ
    - テストデータを利用した推論
    - Strech goal
        - ノーコードデプロイメント
        - ハイパーパラメータチューニング

- 参考
    - [azure-machine-learning-quickstarts](https://github.com/solliancenet/azure-machine-learning-quickstarts)
    - [machine-learning-quickstarts](https://github.com/solliancenet/machine-learning-quickstarts)
    - [azure-machine-learning-service-labs](https://github.com/solliancenet/azure-machine-learning-service-labs)
    - [Azure-Machine-Learning-Dev-Guide](https://github.com/solliancenet/Azure-Machine-Learning-Dev-Guide)


# Backup
- **Module 0 : 環境準備**
    - Azure Machine Learning ワークスペース作成
    - Notebook VM (Compute Instance) 作成
    - Training Cluster 作成

- **Module 1 : 機械学習概論 & Azure Machine Learning ご紹介**
    - 機械学習概論
    - Azure Machine Learning 概要

- **Module 2 : 自動機械学習 Automated ML ハンズオン**
    - データのダウンロード
    - データセット登録
    - Azure ML studio による自動機械学習
    - 結果の解釈
- **Module 3 : 自動機械学習 機械学習モデルの解釈 ハンズオン**
    - Notebook VM の起動
    - Python SDK による自動機械学習
    - モデルの解釈

- **Module 4 : モデルのデプロイと運用 ハンズオン**
    - 自動機械学習モデルのデプロイ
    - テストデータを利用した推論

<figure>
<iframe src="//www.slideshare.net/slideshow/embed_code/key/EixD8OUMBX65Jy" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe>
</figure>

# 環境準備

### 必要なもの

- クライアントPC
- ブラウザ : [Microsoft Edge](https://www.microsoft.com/en-us/edge) or Chrome
- Azure Subscription
    - 共同作成者 (※難しい場合は個人アカウントを準備ください)

<br>

### Azure Machine Learning セットアップ

Azure Machine Learning Workspace をセットアップします。詳細な手順については、下記チュートリアルをご参照ください。

- Azure Machine Learning  の環境構築とチュートリアル<br>
・ [チュートリアル:Python SDK で初めての ML 実験を作成する](https://docs.microsoft.com/ja-JP/azure/machine-learning/service/tutorial-1st-experiment-sdk-setup)<br>
・ [チュートリアル: 最初の ML モデルをトレーニングする](https://docs.microsoft.com/ja-JP/azure/machine-learning/service/tutorial-1st-experiment-sdk-train)

※ 価格レベルは、**Enterprise Edition** を選択してください。

[ml.azure.com](ml.azure.com) にアクセスして、統合開発環境 Azure Machine Learning studio の画面が表示されることを確認します。


<br>

### スキル

ある程度の機械学習や Python の知識も必要になります。普段あまり機械学習に触れていない方は下記のトレーニングコースをご参照ください。

- Aidemy 無償トレーニングコース
    - [機械学習概論](https://aidemy.net/courses/2010)
    - [Python入門](https://aidemy.net/courses/3010)


## Reference
- [自動機械学習とは？ (製品ドキュメント)](https://docs.microsoft.com/ja-JP/azure/machine-learning/service/concept-automated-ml?WT.mc_id=oreilly-webinar-lazzeri)
- [アウトプットの理解 (製品ドキュメント)](https://docs.microsoft.com/ja-jp/azure/machine-learning/service/how-to-understand-automated-ml)
- [モデル解釈可能性 (製品ドキュメント)](https://docs.microsoft.com/ja-JP/azure/machine-learning/service/how-to-machine-learning-interpretability)
- [Automated ML Sample Notebook (Microsoft Official)](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/automated-machine-learning)
- [Probabilistic Matrix Factorization for Automated Machine Learning (Microsoft Research AutoML Meta Learning)](https://www.microsoft.com/en-us/research/publication/probabilistic-matrix-factorization-for-automated-machine-learning/)

- [Interpret-Community (Interpret Library by Microsoft)](https://github.com/interpretml/interpret-community)

- [Interpretable Machine Learning (General Guidance)](https://christophm.github.io/interpretable-ml-book/)

- [機械学習モデル解釈ナイト (DLLAB)](https://dllab.connpass.com/event/153453/)
