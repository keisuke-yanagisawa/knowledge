タンパク質立体構造を使ったDeep learning手法

## タンパク質-化合物 結合予測

### 3DCNN
* AtomNet [[Wallach+2015]](https://arxiv.org/abs/1510.02855) at arXiv
  * データセット：DUDE, ChEMBL-20 PMD (1uM以下の阻害剤をまとめたもの)
* gnina [[Ragoza+2017]](https://pubs.acs.org/doi/abs/10.1021%2Facs.jcim.6b00740) [[Hochuli+2018]](https://www.sciencedirect.com/science/article/pii/S1093326318301670) [[Sunseri+2019]](https://link.springer.com/article/10.1007/s10822-018-0133-y)
  * Univ. Pittsburgh の [David Ryan Koes](http://bits.csb.pitt.edu/) グループ
    * smina を作ったグループ（人？）っぽい。だからsminaと似た名前なのかな。
  * コードやウェブサーバなど：https://github.com/gnina/gnina
  * データセット：CSAR, DUD-E
  * 目的変数：回帰予測の結果を利用した阻害剤の結合ポーズ予測 (CSAR) と分類予測による阻害剤予測 (DUD-E) 
* KDEEP [[Jimenez+2018]](https://pubs.acs.org/doi/10.1021/acs.jcim.7b00650)
  * Univ. Pompeu Fabra (Barcelona) の [Gianni De Fabritiis](http://www.compscience.org/) グループ
  * コードやウェブサーバなど：[PlayMolecule](https://playmolecule.org/) 、オープンソースではなさそう
  * データセット：CSAR, BindingMOAD, PDBbind
  * 目的変数：結合親和性（pIC50やpKi、pKdの値）の回帰予測
* Pafnucy(?) [[Stepniewska-Dziubinska+2018]](https://academic.oup.com/bioinformatics/article/34/21/3666/4994792)
  * Polish Academy of Science の [Pawel Siedlecki](https://cheminfibb.github.io/) グループ
  * コードやウェブサーバなど：https://gitlab.com/cheminfIBB/pafnucy
  * データセット：PDBbind (v.2016), CASF-2013
  * 目的変数：結合親和性（pIC50やpKi、pKdの値）の回帰予測

<!--
* NAME [[AUTHOR YEAR]](ADDRESS) at JOURNAL NAME
  * INSTITUTE NAME の PRINCIPAL INVESTIGATOR グループ
  * コードやウェブサーバなど：存在すればアドレスを記述
  * データセット：
  * 目的変数：
  * 推しポイント（あれば）
-->

### それ以外
* OnionNet [[Zheng+2019]](https://arxiv.org/abs/1906.02418) at arXiv
  * データセット：PDBbind, CASF-2013
  * 目的変数：pKa, pIC50など、活性値
  * 推しポイント：各原子？各残基？から半径K以内の原子数をカウントする構造（だからOnion）なので、回転不変（FEATUREにめっちゃ似てるなぁ）

## タンパク質 結合予測関係

### 3DCNN
* DeepSite [[Jimenez+2017]](https://academic.oup.com/bioinformatics/article/33/19/3036/3859178)
  * Univ. Pompeu Fabra (Barcelona) の Fabritiis グループ
    * ところでこの人は Acellera というスピンオフ企業も持っている
  * [PlayMolecule](https://playmolecule.org/) にweb serverが存在、オープンソースではなさそう
  * タンパク質の結合ポケット部位予測
* LigVoxel [[Skalic+2019]](https://academic.oup.com/bioinformatics/article/35/2/243/5050023)
  * Univ. Pompeu Fabra (Barcelona) の Fabritiis グループ
  * [PlayMolecule](https://playmolecule.org/) にweb serverが存在、オープンソースではなさそう
  * 結合ポケットのPharmacophoreのようなものを描画する
* DeepDrug3D [[Pu+2019]](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1006718)
  * タンパク質の結合ポケットの分類 
* [[Torng&Altman2018]](https://academic.oup.com/bioinformatics/article/35/9/1503/5104336)
  * タンパク質機能部位予測

## タンパク質構造安定性

* 3DCNN_MQA [[Derevyanko+2018]](https://academic.oup.com/bioinformatics/article/34/23/4046/5040325)
  * タンパク質全体を帯域3DCNN
* Ornate [[Pages+2019]](http://dx.doi.org/10.1093/bioinformatics/btz122)
  * 残基単位で局所3DCNN
  
## その他のタンパク質立体構造関係


