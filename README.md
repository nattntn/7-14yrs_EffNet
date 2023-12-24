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

## Google Drive
* **Transfer and Fine-tune with Duo (7-14 years)**
  * [Drive: Model --> Unflipped_Multi_task(7-14))](https://drive.google.com/drive/u/0/folders/1VtMGbAGY-p9oDw0X5pwFXr79_T6_r7r1)

* **Transfer and Fine-tune with Age (7-14 years)**
  * [Drive: Model --> Unflipped_Regress_Age(7-14)](https://drive.google.com/drive/u/0/folders/1lThC7Ft1dU3_4gGOPXNezZJJOwTLpZV5)
* **Transfer with Age and Fine-tune with Duo (7-14 years)**
  * [Drive: Model --> Unflipped_Regress_Age(7-14)--> Duo](https://drive.google.com/drive/u/0/folders/1QxEWQw5nV6Ue5J7Ink2qT29hvqTku26A)

* **Transfer and Fine-tune with Gender (7-14 years)**
  * [Drive: Model --> Unflipped_Classification_Gender(7-14)](https://drive.google.com/drive/u/0/folders/1gSnNTp_DwS-gacctGDKAy0MGtKOMxsEk)

## Results (7-14 yrs)
|  Transfer learning  | Fine-tuning  | Age (RMSE)  | Gender(Accuracy)  |  Age (R^2) | Epochs |
| :------------------:|:------------:|:-----------:|:-----------------:|:----------:|:------:|
|         Duo         |      -       |     1.16    |      68.62%       |   74.00%   |  3,500 |
|         Duo         |    Duo(22)   |     0.93    |      81.63%       |   83.38%   |  2,000 |
|         Duo         |    Duo(32)   |     0.94    |      77.30%       |   82.94%   |  4,500 |
|         Age         |       -      |     1.18    |        -          |   73.41%   |  3,500 |
|         Age         |      Duo     |     0.94    |      75.51%       |   82.89%   |  3,500 |
|       Gender        |       -      |      -      |      65.05%       |     -      |  2,500 |
|       Gender        |      Duo     |     0.96    |      77.30%       |   82.26%   |  4,500 |

