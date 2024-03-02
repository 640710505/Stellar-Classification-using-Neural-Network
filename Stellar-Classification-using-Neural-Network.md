
# Data Visualization
# 
#
![Unknown](https://github.com/640710505/Sellar-Classification-using-Neural-Network/assets/114089025/e5c9f836-24ab-4d1e-b257-d0c5f782256a)
#
![Unknown](https://github.com/640710505/Sellar-Classification-using-Neural-Network/assets/114089025/dfadc634-c486-4f6f-9fa8-3cad6e3d14b0)
#
![Unknown](https://github.com/640710505/Stellar-Classification-using-Neural-Network/assets/114089025/9c0a3c05-6f9e-453e-a80d-01a776fe7405)
#
# 
#
#

# Feature important 
### With Logistic Regression

```python
### All feature and Target(class)  
X = data[['obj_ID','alpha', 'delta', 'u', 'g', 'r', 'i', 'z', 'run_ID',
       'rerun_ID', 'cam_col', 'field_ID', 'spec_obj_ID', 'redshift',
       'plate', 'MJD', 'fiber_ID']]
Y = data[['class']]
```
```python
###  use train_test_split  by train 70 % and test 30%
from sklearn.model_selection import train_test_split
X_train,X_test,Y_train,Y_test = train_test_split(X,Y,test_size=0.3, 
                                                 random_state=42,
                                                 shuffle 
                                                 = True,stratify= Y)
```
```python
### Use StandardScaler for scaling data to samesame  value 
from sklearn.preprocessing import StandardScaler
sc = StandardScaler()
sc.fit(X)
X_train_std = sc.transform(X_train)
X_test_std = sc.transform(X_test) 
```
```python
### test Model
model = LogisticRegression()
model.fit(X_train_std,Y_train)
```
```python
model.score(X_test_std,Y_test)
```
<details>
<summary><strong>Output</strong></summary>

```
0.948473816858023
```
</details>

```python
print(coefficients)
```
<details>
  <summary><strong>Output</strong></summary>

```
[[ 1.45477542e-02 -1.23103249e-02 -4.53120066e-02  7.01904752e+00
   4.68105844e+00  1.04455625e+00 -1.55975245e+00 -9.38051743e-01
   1.45520219e-02  0.00000000e+00 -4.32997959e-02  4.53115258e-02
   3.21639936e-01  1.47975574e+01  3.21640912e-01 -7.00410253e-01
   3.47263277e-02]
 [ 2.28612863e-02  8.05451884e-02  1.89388215e-01 -8.30274338e+00
  -2.64094232e+00 -2.85728341e+00  2.66957060e+00  5.55446057e+00
   2.28643623e-02  0.00000000e+00 -3.14602773e-02  2.28082408e-02
  -9.72926616e-02  1.94403139e+01 -9.72935111e-02 -7.41901037e-02
   1.46102515e-02]
 [-3.74090405e-02 -6.82348635e-02 -1.44076209e-01  1.28369587e+00
  -2.04011611e+00  1.81272715e+00 -1.10981815e+00 -4.61640883e+00
  -3.74163842e-02  0.00000000e+00  7.47600732e-02 -6.81197666e-02
  -2.24347275e-01 -3.42378713e+01 -2.24347401e-01  7.74600357e-01
  -4.93365792e-02]]
```
</details>

## Coefficient Graph
![featureimportant](https://github.com/640710505/Sellar-Classification-using-Neural-Network/assets/141728733/10905af0-4587-4fcf-bc27-d759f84fc7d1)
# 
#
#
# Feature Extraction
#
#
# 



#
#
# 
#
# Neural Network Model
# 
#
#
# 
#
#
# 
#
# Score Analysis
# 

