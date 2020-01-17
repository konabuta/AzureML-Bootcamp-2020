## Interpretability Community

Azure Machine Learning service が提供するモデル解釈ライブラリ。機械学習モデルのモデル全体の説明変数の重要度 (グローバル) や個々の予測値に対する説明変数の重要度 (ローカル) を理解することが可能です。

### 基本コンポーネント

<img src="https://docs.microsoft.com/ja-jp/azure/machine-learning/service/media/machine-learning-interpretability-explainability/interpretability-architecture.png" width=600><br/>

今回は **Tabulear Data (表形式データ)** について説明します。<br/>


### Mimic
**Global Surrogate** に対応する Explainer です。

Azure Machine Learning では、`LightGBM` `Linear Regression` `SGD` `Decision Tree` が利用できます。

```python
from azureml.explain.model.mimic.mimic_explainer import MimicExplainer

# you can use one of the following four interpretable models as a global surrogate to the black box model
from azureml.explain.model.mimic.models.lightgbm_model import LGBMExplainableModel
from azureml.explain.model.mimic.models.linear_model import LinearExplainableModel
from azureml.explain.model.mimic.models.linear_model import SGDExplainableModel
from azureml.explain.model.mimic.models.tree_model import DecisionTreeExplainableModel

explainer = MimicExplainer(model, 
                           x_train, 
                           LGBMExplainableModel, 
                           augment_data=True, 
                           max_num_of_augmentations=10, 
                           features=breast_cancer_data.feature_names, 
                           classes=classes)
```
<br/>

### Feature Permutation
**Permutation Feature Importance** に対応する Explainer です。

```python
from azureml.explain.model.permutation.permutation_importance import PFIExplainer 

# "features" and "classes" fields are optional
explainer = PFIExplainer(model, 
                         features=breast_cancer_data.feature_names, 
                         classes=classes)
```

<br/>

### Tabular Explainer (SHAP)

**SHAP** に対応する Explainer です。
- ツリーベースのモデルの場合は、_SHAP TreeExplainer_ を適用
- DNN モデルの場合は、_SHAP DeepExplainer_ を適用
- BlackBox モデルとして扱う場合は、_SHAP KernelExplainer_ を適用

```python
from azureml.explain.model.tabular_explainer import TabularExplainer
# "features" and "classes" fields are optional
explainer = TabularExplainer(model, 
                             x_train, 
                             features=breast_cancer_data.feature_names, 
                             classes=classes)
```
