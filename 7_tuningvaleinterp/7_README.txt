Aqui van a hacer los respectivos modelos usando los metodos de validacion cruzada respectivos:

• Tuning de hiperparametros: uso obligatorio de sklearn.Pipeline con GridSearchCV, BayesSearchCV u Optuna.
• Validacion cruzada: StratifiedKFold (clasificacion) o KFold (regresion), mınimo 5 folds.
• Interpretabilidad: aplicar en los tres mejores modelos usando feature importances ,Coeficientes, SHAP o Permutation Importance.

En cada carpeta colocan el .ipynb y cuando este listo, lo marcan con X al final, o lo ponen cuando hagan commit.

Modelos faltantes:

- [] KNN 
- [] Bayes
- [] LogRes (L1/L2)
- [] Arboles
- [] RandomForest
- [] XGB
- [] SVM

Por esta seccion, solo se hace el modelo normal sin ningun tipo de validacion.
Los modelos deben tener sus respectivos analisis y metricas:

- Matriz de confusion
- ROC-AUC
- Tabla de Accuracy, f1-score, precision

Al final, cuando se tengan todos los modelos listos, se colocaran en el 7_tuningvaleinterp