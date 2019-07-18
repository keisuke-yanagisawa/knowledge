タンパク質の立体構造を使わないdeep learning手法のまとめ
（主に配列ベースの手法になっている気がする）


* DeepCSeqSite [[Cui+2019]](https://doi.org/10.1186/s12859-019-2672-1)
  * タンパク質配列からリガンド結合残基予測、1DCNN
* DeepSF [[Hou+2018]](https://academic.oup.com/bioinformatics/article/34/8/1295/4708302)
  * タンパク質配列からfold予測（分類問題）、1DCNN
* SPOT-1D [[Hanson+2019]](https://doi.org/10.1093/bioinformatics/bty1006)
  * 予測されたコンタクトマップを使うことで二次構造予測、主鎖角度予測、ASA予測、近隣原子数予測の精度を向上
  * LSTM-BRNNを利用
