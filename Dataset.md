化合物やタンパク質などなどのデータセットについてまとめてみる。

## 総合
- NCBI [BioSample](https://www.ncbi.nlm.nih.gov/biosample/)
  - 実験データがいろいろまとまっている雰囲気（よくしらない）
  - たとえばメタゲノムの[WGSデータ](https://www.ncbi.nlm.nih.gov/genbank/wgs/)とか

## 化合物-タンパク質系

### 立体構造あり
- [PDB](https://www.rcsb.org/)
- PDBbind
  - PDBに登録されている、阻害活性などが判明しているPDBエントリなどをまとめている2次データ。
  - 最近ずっとリンク切れしている気がする。
- [scPDB](http://bioinfo-pharma.u-strasbg.fr/scPDB/)
  - PDBから結合部位を切り出してまとめた2次データ（PDBbindと何が違うんだろう、ちゃんと理解してないや）
- [DUD](http://dud.docking.org/), [DUD-E](http://dude.docking.org/)
- [BioLip](https://zhanglab.ccmb.med.umich.edu/BioLiP/)
- [MetalPDB](http://metalweb.cerm.unifi.it/)
  - 金属イオンが結合するタンパク質に関する二次データベース。これは化合物-タンパク質に分類していいのかわからないけれど。

### 立体構造なし
- [PubChem](https://pubchem.ncbi.nlm.nih.gov/) BioAssay
- [ChEMBL](https://www.ebi.ac.uk/chembl/)
- [ATPbind](https://zhanglab.ccmb.med.umich.edu/ATPbind/)
  - [[Hu+2018, JCIM]](https://pubs.acs.org/doi/10.1021/acs.jcim.7b00397) の研究成果。


## 化合物系

### QM系
- [QM dataset](http://quantum-machine.org/datasets/)
  - QM7, QM7b
  - QM8
  - QM9
  - ISO17
- [ANI1](https://figshare.com/collections/_/3846712)

### その他
- [ZINC](http://zinc.docking.org/), [ZINC15](https://zinc15.docking.org/)
- [Tox21](https://tox21.gov/)
- [COMDECOM](https://journals.sagepub.com/doi/abs/10.1177/1087057109336953)
- [SIDER](http://sideeffects.embl.de/)
- [LINCS](http://www.lincsproject.org/)
- [[He+2019, IJMS]](https://www.mdpi.com/1422-0067/20/8/1897)
- [[Furukawa+2016]](https://pubs.acs.org/doi/abs/10.1021/acs.jmedchem.6b01246)
- [[Ingle+2016, JCIM]](https://pubs.acs.org/doi/10.1021/acs.jcim.6b00291)
  - ヒト血漿タンパク質結合率をまとめて予測を行った論文で、データが公開されている。

## タンパク質系

### 立体構造系
- [PDB](https://www.rcsb.org/)
  - APO体も多く登録されているので再登場
- [CASP](http://predictioncenter.org/)
- [EMDataResource](https://www.emdataresource.org/index.html)

### 配列情報系
- [UniProt](https://www.uniprot.org/)

## その他

### 医療画像
- [TCIA](https://www.cancerimagingarchive.net/)
