タンパク質立体構造を使ったDeep learning手法

## タンパク質-化合物 結合予測

### 3DCNN
* AtomNet [[Wallach+2015]](https://arxiv.org/abs/1510.02855) at arXiv
  * データセット：DUDE, ChEMBL-20 PMD (1uM以下の阻害剤をまとめたもの)
* [[Ragoza+2017]](https://pubs.acs.org/doi/abs/10.1021%2Facs.jcim.6b00740)
* KDEEP [[Jimenez+2018]](https://pubs.acs.org/doi/10.1021/acs.jcim.7b00650)
* [[Stepniewska-Dziubinska+2018]](https://academic.oup.com/bioinformatics/article/34/21/3666/4994792)
* [[Hochuli+2018]](https://www.sciencedirect.com/science/article/pii/S1093326318301670)
* [[Sunseri+2019]](https://link.springer.com/article/10.1007/s10822-018-0133-y)

### それ以外
* OnionNet [[Zheng+2019]](https://arxiv.org/abs/1906.02418) at arXiv
  * データセット：PDBbind, CASF-2013
  * 目的変数：pKa, pIC50など、活性値
  * 推しポイント：各原子？各残基？から半径K以内の原子数をカウントする構造（だからOnion）なので、回転不変

## タンパク質 結合部位予測

## タンパク質構造安定性

## その他のタンパク質立体構造関係

* LigVoxel [[Skalic+2019]](https://academic.oup.com/bioinformatics/article/35/2/243/5050023)
* タンパク質の結合ポケットの分類 [[Pu+2019]](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1006718)

