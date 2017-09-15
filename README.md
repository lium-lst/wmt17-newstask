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

[Download (13M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/setimes2.norm.min3max50.tok.tar.bz2) our normalized/tokenized/length-filtered version of officially provided [SETIMES2](http://opus.lingfil.uu.se/SETIMES2.php) with ~200K sentences.

#### Back-translations

[Download (96M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/news2016-BT-EN-TR.tar.bz2)
incremental subsamples of 150K, 700K and 1M parallel back-translation corpora
where the target(TR) side samples are from monolingual Turkish data [`news.2016.shuffled`](http://data.statmt.org/wmt17/translation-task/news.2016.tr.shuffled.gz). The sentences are translated into EN with a single TR->EN NMT system (~14 BLEU on newstest2016).
