化合物のDeep learning機械学習手法全般。

## 全結合系

* [[Wenzel+2019]](https://doi.org/10.1021/acs.jcim.8b00785)
  * 特徴量：Dragon, MOE, RDKitで作られた様々な特徴量 (e.g. Physicochemical properties, structural information, fragment information)
  * 予測対象：ADME-Toxデータ（受動膜透過、logD、動物実験データ）
  * マルチタスク学習 ☑
  
## Graph Convolution系
* kCON [[Chen+2018]](https://pubs.acs.org/doi/10.1021/acs.jctc.8b00149)
  * 予測対象：量子化学計算による原子単位に定義される値（雑）
* Chemi-Net [[Liu+2019]](https://www.mdpi.com/1422-0067/20/14/3389)
  * Graph convolution：InceptionとWeave moduleを参考にしたとのこと（4.2節）
  * 予測対象：Solubility, Bioavailabilityなど、薬剤化合物のADME特性
  * マルチタスク学習 ☑
  
<!--
テンプレート
* [[NAME+YYYY]](ARTICLE ADDRESS)
  * 特徴量：
  * 予測対象：
  * マルチタスク学習 ☑ or □ 
  * 推しポイント：
-->
