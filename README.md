# LIUM WMT17 Systems for News Translation Task

Below you will find the data and [nmtpy](https://github.com/lium-lst/nmtpy) configurations for LIUM's WMT17 News Translation systems (see [paper](http://www.aclweb.org/anthology/W17-4726.pdf)):

```
@InProceedings{garciamartinez-EtAl:2017:WMT,
  author    = {Garc\'{i}a-Mart\'{i}nez, Mercedes  and
               Caglayan, Ozan  and  Aransa, Walid
               and  Bardet, Adrien  and  Bougares, Fethi
               and  Barrault, Lo\"{i}c},
  title     = {LIUM Machine Translation Systems for WMT17 News Translation Task},
  booktitle = {Proceedings of the Second Conference on Machine Translation, Volume 2: Shared Task Papers},
  month     = {September},
  year      = {2017},
  address   = {Copenhagen, Denmark},
  publisher = {Association for Computational Linguistics},
  pages     = {288--295},
  url       = {http://www.aclweb.org/anthology/W17-4726.pdf}
}
```

## En->Tr Systems

### Data

(Note: Turkish side of the corpora below is tokenized with a [slightly modified version](scripts/tokenizerv2.perl) of Moses tokenizer which handles apostrophes correctly for Turkish.)

- [Download (13M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/setimes2.norm.min3max50.tok.tar.bz2) our normalized/tokenized/length-filtered version of officially provided [SETIMES2](http://opus.lingfil.uu.se/SETIMES2.php) with ~200K sentences.

- [Download](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/en-tr-16k.bpe) joint BPE (16K merge ops) trained on bitext.

- **The exact** incremental subsamples of 150K, 700K, 1M and 1.7M (~all news2016) parallel back-translation corpora used in the **paper** where the target (TR) side samples are from monolingual Turkish data [`news.2016.shuffled`](http://data.statmt.org/wmt17/translation-task/news.2016.tr.shuffled.gz). The sentences are translated into EN with a single TR->EN NMT system (~14 BLEU on newstest2016):
  - [Tokenized (187M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/news2016-BT-EN-TR.tar.bz2)
  - [Tokenized+BPE (199M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/news2016-BT-EN-TR-BPE16K.tar.bz2)

- **Ready to use** BPE-ized subsamples as they are used in the paper (cf. Table 3):
  
  - **(System B0)** BPE-ized, (only) SETIMES2-200K (~200K total) [corpora (14M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/only-SETIMES2-200K.tar.bz2)
  - **(System B1)** BPE-ized, (only) BT-1M (~1M total) [corpora (58M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/only-BT-1M.tar.bz2)
  - **(System B2)** BPE-ized, SETIMES2-200K+BT-150K (~350K total) [corpora (21M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/SETIMES2-200K+BT-150K.tar.bz2)
  - **(System B4)** BPE-ized, SETIMES2-200K+BT-700K (~900K total) [corpora (51M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/SETIMES2-200K+BT-700K.tar.bz2)
  - **(System B6)** BPE-ized, SETIMES2-200K+BT-1M (~1.2M total) [corpora (72M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/SETIMES2-200K+BT-1M.tar.bz2)
  - **(System B8)** BPE-ized, SETIMES2-200K+BT-1.7M (~1.9M total) [corpora (112M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/SETIMES2-200K+BT-1.7M.tar.bz2)
  
