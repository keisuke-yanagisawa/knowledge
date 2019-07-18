化合物のDeep learning機械学習手法全般。

## Classification / Regression

### 全結合系

* [[Wenzel+2019]](https://doi.org/10.1021/acs.jcim.8b00785)
  * 特徴量：Dragon, MOE, RDKitで作られた様々な特徴量 (e.g. Physicochemical properties, structural information, fragment information)
  * 予測対象：ADME-Toxデータ（受動膜透過、logD、動物実験データ）
  * マルチタスク学習 ☑
* DeepPharm [[Ye+2019]](https://doi.org/10.1021/acs.molpharmaceut.8b00816)
  * まずQSARタスクでネットワークのPre-trainを行い、ADMETに関する複数の値のマルチタスク学習を行う。
  * [ ] 要確認事項：化合物の特徴量は何を使っている？本文を見ないとわからない
  
### Graph Convolution系
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


## Generative model

* [[Stahl+2019]](https://pubs.acs.org/doi/10.1021/acs.jcim.9b00325)
  * 深層強化学習による薬剤設計
  * Bidirectional LSTMを利用（SMILESベースか？調べる必要あり）
* [[Sattarov+2019]](https://pubs.acs.org/doi/10.1021/acs.jcim.8b00751)
  * SMILESベースのAutoencoder
  * Bidirectional LSTMを利用
  * Generative Topographic Mappingを使うことでLatent spaceを2次元に可視化、範囲をユーザーが指定できるようにしている？
* [[Skalic+2019]](https://pubs.acs.org/doi/10.1021/acs.jcim.8b00706)
  * SMILESだけでなく立体構造を意識する深層学習分子設計手法
  * Autoencoderを用いてシード化合物のSMILESからShape representationを作成、そのShape representationから新しい化合物のSMILESを生成する
* [[Awale+2019]](https://pubs.acs.org/doi/10.1021/acs.jcim.8b00902)
  * 転移学習×Generative model？
  * 詳細全然読んでいない

## Applicable domain / Reliability 等

* [[Cortes-Ciriano&Bender2019]](https://doi.org/10.1021/acs.jcim.9b00297)
  *  ECFP4を特徴量とするDense DNNにおいて、推論時に（学習時ではない）Dropoutを起こしたときにどの程度予測結果が変化するか、という評価を行うことで予測結果のReliabilityを評価

<!--
テンプレート
* [[NAME+YYYY]](ARTICLE ADDRESS)
  * 特徴量：
  * 予測対象：
  * マルチタスク学習 ☑ or □ 
  * 推しポイント：
-->
