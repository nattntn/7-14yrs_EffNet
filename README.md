# 7-14yrs_EffNet
Unflipped training using panoramic radiograph images of patients aged between 7-14 yrs.

**Training Dataset**

|  Age  | Male(People)  | Female(People)  | Sum(People)  |  Sum(Images) |
| ------|:-------------:|:---------------:|:------------:|:------------:|
|  7    |      61       |       61        |      122     |      225     |
|  8    |      63       |       58        |      121     |      232     |
|  9    |      61       |       62        |      123     |      242     |
|  10   |      57       |       58        |      115     |      230     |
|  11   |      59       |       62        |      121     |      231     |
|  12   |      60       |       63        |      123     |      236     |
|  13   |      58       |       54        |      112     |      214     |
|  14   |      62       |       57        |      119     |      223     |
|**Sum**|    **xxx**    |    **xxxxx**    |   **xxxxx**  |   **xxxxx**  |

## Google Drive ⚓
* **Transfer and Fine-tune with Duo (7-14 years)**
  * [Drive: Model --> Unflipped_Multi_task(7-14))](https://drive.google.com/drive/u/0/folders/1VtMGbAGY-p9oDw0X5pwFXr79_T6_r7r1)
  * [Predict R22:colab](https://colab.research.google.com/drive/1CC185wjhqY2s9hWtenLgRc2JxbPF97S-?usp=sharing)
  * [Predict R32:colab](https://colab.research.google.com/drive/1iqXKPUtGcq4-26rt2vHpnX5i4z2mW2YK?usp=sharing)
  * [Predict R36:colab](https://colab.research.google.com/drive/1wpLRRrBU9Bcs_l3r-L-j8NXwSzSHBTNP?usp=sharing) : ใช้แยกอายุน้อย

* **Transfer with Age and Fine-tune with Duo (7-14 years)**
  * [Drive: Model --> Unflipped_Regress_Age(7-14)](https://drive.google.com/drive/u/0/folders/1lThC7Ft1dU3_4gGOPXNezZJJOwTLpZV5)
  * [Predict](https://colab.research.google.com/drive/1NgLHqNlUcADdpqaqs_lD0YlYNBnb-4Ti#scrollTo=RncttvaPKd3r)

* **Transfer with Gender and Fine-tune with Duo (7-14 years)**
  * [Drive: Model --> Unflipped_Classification_Gender(7-14)](https://drive.google.com/drive/u/0/folders/1gSnNTp_DwS-gacctGDKAy0MGtKOMxsEk)
  * [train R28](https://colab.research.google.com/drive/1jihTHoMGzAm6iZ7pxQc--9GUbkLUhvOK)
  * [predict R28](https://colab.research.google.com/drive/1uk-pX4wqktpR5dAXVF6wF5_kbXX6ofu3?usp=sharing)

## Results (7-14 yrs)
|  Transfer learning  | Fine-tuning  | Age (RMSE)  | Gender(Accuracy)  |  Age (R^2) |  ROC   | Epochs |
| :------------------:|:------------:|:-----------:|:-----------------:|:----------:|:------:|:------:|
|         Duo         |      -       |     1.16    |      68.62%       |   74.00%   |   -    |  3,500 |
|         Duo         |    Duo(22)   |     0.93    |      81.63%       |   83.38%   |**0.87**|  2,000 |
|         Duo         |    Duo(32)   |   **0.94**  |      77.30%       | **82.94%** |  0.86  |  4,500 |
|         Duo         |    Duo(36)   |     0.95    |    **79.85%**     |   82.84%   |**0.87**|  x,xxx |
|         Age         |       -      |     1.18    |        -          |   73.41%   |   -    |  3,500 |
|         Age         |      Duo     |   **0.94**  |      75.51%       |   82.89%   |  0.86  |  3,500 |
|       Gender        |       -      |      -      |      65.05%       |     -      |   -    |  2,500 |
|       Gender        |      Duo     |     0.96    |      77.30%       |   82.26%   |  0.85  |  4,500 |

