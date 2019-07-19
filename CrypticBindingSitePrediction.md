Cryptic Binding Siteの予測手法の整理。
Machine Learning ディレクトリとの情報の重複があるかも。
<!-- TEMPLATE
* NAME [[AUTHOR YEAR]](ADDRESS) at JOURNAL NAME
  * INSTITUTE NAME の PRINCIPAL INVESTIGATOR グループ
  * コードやウェブサーバなど：存在すればアドレスを記述
  * データセット：
  * 目的変数：
  * 推しポイント（あれば）
-->

## レビュー論文など
* Cryptic binding sites on proteins: definition, detection, and druggability [[Vajda+2018]](https://doi.org/10.1016/j.cbpa.2018.05.003) at Current Opinion in CHemical Biology
  * 半ば [[Beglov+2018]](http://www.pnas.org/lookup/doi/10.1073/pnas.1711490115)の宣伝論文ではあるが、この分野において静的構造からの予測は（汎用手法を除いて）行われていないことが良くわかる資料になっている。

## MD系手法（予測よりも観測を重視）
* [[Bowman & Geissler 2012]](https://www.pnas.org/content/109/29/11681) at PNAS
  * MSMを使ったMD計算（合計数百us）を行うことでCrypticなサイトの構造変化を誘発させる。
  * 3つのタンパク質（beta-lactamase, interleukin-2, RNase）を対象とした実験を行った。

## Cosolvent MD手法（Hot Spot解析）
省略（MixMD, SILCS, MDMixあたりとか）

## 機械学習系手法
  
* MDpocket [[Schmidtke+2011]](https://academic.oup.com/bioinformatics/article-lookup/doi/10.1093/bioinformatics/btr550) at Oxford Bioinformatics
* CryptoSite [[Cimermancic+2016]](https://www.sciencedirect.com/science/article/pii/S0022283616000851) at JMB
  * UCSF の [Andrej Sali](https://salilab.org/) グループ
  * コードやウェブサーバなど：[コード](https://github.com/salilab/cryptosite/)/[ウェブサーバ](https://modbase.compbio.ucsf.edu/cryptosite/)
  * データセット：
  * 目的変数：
* DeepSite [[Jimenez+2017]](https://academic.oup.com/bioinformatics/article/33/19/3036/3859178) at Oxford Bioinformatics
  * [MachineLearning/Protein3DStructureDL.md](https://github.com/keisuke-yanagisawa/knowledge/blob/master/MachineLearning/Protein3DStructureDL.md) に記述済み 
