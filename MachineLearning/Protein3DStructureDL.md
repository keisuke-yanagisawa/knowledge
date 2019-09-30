タンパク質立体構造を使ったDeep learning手法
<!--
* NAME [[AUTHOR YEAR]](ADDRESS) at JOURNAL NAME
  * INSTITUTE NAME の PRINCIPAL INVESTIGATOR グループ
  * コードやウェブサーバなど：存在すればアドレスを記述
  * データセット：
  * 目的変数：
  * 推しポイント（あれば）
-->
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


### それ以外
* OnionNet [[Zheng+2019]](https://arxiv.org/abs/1906.02418) at arXiv
  * データセット：PDBbind, CASF-2013
  * 目的変数：pKa, pIC50など、活性値
  * 推しポイント：各原子？各残基？から半径K以内の原子数をカウントする構造（だからOnion）なので、回転不変（FEATUREにめっちゃ似てるなぁ）
* [[Gonczarek+2018]](https://www.sciencedirect.com/science/article/pii/S0010482517302974)
  * [Alphamoon Ltd.](https://alphamoon.ai/) の研究。純粋にDS/AIやってるコンサル企業のようにも見える。
  * データセット：DUD-E, DUD, PDBBind, MUV
  * 入力：タンパク質と化合物のドッキングポーズ、タンパク質はポケット周辺のみ切り出す
  * 学習手法：Neural FingerprintおGraph Convolutionの2つを試した。
    * グラフのノードはタンパク質と化合物の各原子（原子種ごと、タンパク質と化合物別のone-hot-vector）
    * グラフのエッジは一定距離（5A）よりも近い原子ペアに付与。結合だとタンパク質と化合物との間にエッジがはれないから。
  * 目的変数：入力された単一のポケット（タンパク質の一部を切り出したもの）と単一の小分子が、結合するか否かの分類問題
  * 結果：Neural Fingerprintを使ったもので予測を行うと、AutoDock VinaやSminaなどのドッキングそのままよりも精度が向上（DUD-E, MUVどちらも）。
    * いや、機械学習ベースの手法と比較しろよーー
* DeepVS [[Pereira+2016]](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.6b00355)
  * 入力：タンパク質と化合物のドッキングポーズ、タンパク質はポケット周辺のみ切り出す
  * 学習手法：原子単位で特徴量抽出を行い、Map poolingをすることで全体の特徴量とする
    * 各原子の初期特徴量に、ドッキングポーズにおける近傍残基などの情報が含まれているのでtarget specificな予測が可能

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
* DeepDrug3D [[Pu+, PLoS CB, 2019]](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1006718)
  * タンパク質の結合ポケットの分類 
  * 入力特徴はpotentialベース。
    * リガンド中心から半径15A以内について、1A voxelに空間分割。タンパク質に衝突していない、タンパク質のconvex hullからはみ出していない空間のみを選抜し、最大の接続している点集合だけを残す。その点群に対して、sybylの原子分類で14種類の原子を選別して、DFIRE potentialを計算して特徴量としてCNNに入力する。
* [[Torng&Altman, Bioinformatics, 2018]](https://academic.oup.com/bioinformatics/article/35/9/1503/5104336)
  * タンパク質機能部位予測

## タンパク質構造安定性

* 3DCNN_MQA [[Derevyanko+2018]](https://academic.oup.com/bioinformatics/article/34/23/4046/5040325)
  * タンパク質全体を大域3DCNN
* Ornate [[Pages+2019]](http://dx.doi.org/10.1093/bioinformatics/btz122)
  * 残基単位で局所3DCNN
* [[Sato&Ishida, PLoS ONE, 2019]](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0221347)
  * 残基単位で局所3DCNN
  * 入力は原子座標ベース。
    * Derevyankoの手法の11種類に3種類を追加
  
## その他のタンパク質立体構造関係

* 3D deep convolutional neural networks foramino acid environment similarity analysis [[Torng&Altman, BMC Bioinform, 2017]](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-017-1702-0)
  * 入力は原子座標ベース
    * Oxygen, Carbon, Nitrogen, Sulfurの4種類（＝4チャネル）の原子の座標を1A^3 voxel表現、範囲は20A - 20A - 20A

