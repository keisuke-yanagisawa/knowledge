Drug Target Interaction (DTI) 関係論文。

## 行列的手法（相互作用行列・タンパク質類似度行列・化合物類似度行列を利用した手法）
* NRLMFβ [[Ban+2019]](https://doi.org/10.1016/j.bbrep.2019.01.008)
  * 東工大 秋山研 伴さんの論文。
  * NRLMFの改良。事前分布としてベータ分布を導入することで周辺タンパク質/化合物のラベルが殆ど存在しない場合の予測精度を改善させる。
* [[Xia+2019]](https://pubs.acs.org/doi/10.1021/acs.jcim.9b00408)
  * Self-Paced Learning with Collaborative Matrix Factorization だそうだ。わっかんないけど。

## 特徴量的手法（タンパク質-化合物ペアを特徴量に変換して学習）
* PKRang [[Suzuki+2018]](https://link.springer.com/article/10.1007%2Fs10015-017-0416-8)
  * 東工大 秋山研 鈴木翔吾さんの論文。
  * タンパク質と化合物で別々にグラム行列を作り、Pairwise kernelによる学習
  * SVMベースのランク学習を行うことでROC-AUC最大化
* DeepConv-DTI [[Lee+2019]](https://doi.org/10.1371/journal.pcbi.1007129)
  * タンパク質配列を1DCNNで特徴量化、それと化合物のFingerPrintのDense結果と組み合わせて予測を実施
  * 直感的な感想：なんか面白くなさそう（こなみ）

  
