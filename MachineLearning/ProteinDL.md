タンパク質の立体構造を使わないdeep learning手法のまとめ
（主に配列ベースの手法になっている気がする）


* DeepCSeqSite [[Cui+2019]](https://doi.org/10.1186/s12859-019-2672-1)
  * タンパク質配列からリガンド結合残基予測、1DCNN
* DeepSF [[Hou+2018]](https://academic.oup.com/bioinformatics/article/34/8/1295/4708302)
  * タンパク質配列からfold予測（分類問題）、1DCNN
* SPOT-1D [[Hanson+2019]](https://doi.org/10.1093/bioinformatics/bty1006)
  * SPIDER3と同じグループの手法
  * 予測されたコンタクトマップを使うことで二次構造予測、主鎖角度予測、ASA予測、近隣原子数予測の精度を向上
  * LSTM-BRNNの手法とResNetの手法を組み合わせたらしい
* DeepRIN [[Fang+2019]](https://doi.org/10.1109/TCBB.2018.2814586)
  * 雑誌：IEEE Trans Comput Biol Bioinform
  * グループ：[Univ. Missouri-Columbia, Yi Shang グループ](http://dslsrv1.rnet.missouri.edu)
    * 同じ人たちが DeepDIN [[Fang+2019]](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.25780) at Proteins も出している。
  * Residual Inception Networkというものを構築。異なる深さのConvolution層を組み合わせたネットワーク構成。複雑だ。
  * 入力特徴量はアミノ酸の物理的特徴量、PSSM、HHBlitsの出力、あと予測した8分類二次構造。
  * タンパク質主鎖のPhi, Psi角度を予測。正確にはsin(phi), sin(psi), cos(phi), cos(psi)の4つの値を予測する。SPIDER3よりも精度良いらしい。
* Brewery [[Torrisi+2020]](https://doi.org/10.1093/bioinformatics/btaa204)
  * 雑誌：Bioinformatics
  * https://github.com/mircare/Brewery これがGithub
  * Input: あんまり詳細載ってないけど、PSI-BLASTあるいはHHblitsの出力を使うようだ。
  * Output: タンパク質配列から以下の4種類を予測
    * 二次構造 (secondary structure; SS)
    * 相対溶媒接触面積 (relative solvent accessibility; RSA)
    * contact density (CD)
    * Structural motifs obtained from clustering of consecutive torsion angles (TA)
* DELPHI [[Li+2020]](https://doi.org/10.1093/bioinformatics/btaa750)
  * 雑誌：Bioinformatics
  * https://github.com/lucian-ilie/DELPHI
  * Input: 3-merやPSI-BLAST PSSM, RSA, propensityなどを利用するらしい。Table 2参照
  * Model: Deep learning (CNN & RNN)
  * Output: タンパク質の相互作用部位予測

| ツール名 | Input ||| Output ||||Github|
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
|       |<strong>Sequence</strong>|<strong>HHblits</strong>|<strong>PSI-BLAST</strong>| <strong>PSA</strong> | <strong>Secondary structure (SS)</strong> | <strong>Contact density (CD)</strong> | <strong>Torsion angle (TA)</strong> ||
|Brewery|One-hot?|✓|✓|✓|✓|✓|✓|https://github.com/mircare/Brewery|

<!--
* [[]]()
  * 雑誌名：
  * グループ：
-->
