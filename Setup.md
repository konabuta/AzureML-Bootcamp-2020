### コードと Python 環境の準備

ワークショップのサンプルコードをダウンロードし、正常に動作する Python パッケージをインストールします。 

1. Python 3.6 以上の [Miniconda](https://conda.io/miniconda.html) をインストールします。 Azure Machine Learning の Notebook VM (or Compute Instances) を利用する場合は不要です。

1. リポジトリをクローンします。
    ```
    git clone https://github.com/konabuta/Automated-ML-Workshop
    ```
1. conda 環境をインストールします。リポジトリに Python の依存関係を示した `environment.yml` ファイルがあるので、これを用いて環境を構築します。
    ```
    conda env create -f environment.yml
    ```
1. conda 環境を有効します。また、 Jupyter のカーネルに登録します。
    ```
    conda activate automl-workshop
    python -m ipykernel install --user --name automl-workshop --display-name "Python (bootcamp)"
    ```
1. Jupyter Notebook のサーバを開始します。Azure Machine Learning の Notebook VM (or Compute Instances) を利用する場合は不要です。

    ```
    jupyter notebook
    ```
1. 準備完了です。