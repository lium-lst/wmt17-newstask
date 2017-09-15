# LIUM WMT17 Systems for News Translation Task

## En->Tr Systems

### Data

#### Provided bi-text

#### Back-translations

- [Download (96M)](http://lium.univ-lemans.fr/~caglayan/wmt17-newstask/news2016-BT-EN-TR.tar.bz2)
incremental subsamples of 150K, 700K and 1M parallel back-translation corpora
where the target(TR) side samples are from monolingual Turkish data [`news.2016.shuffled`](http://data.statmt.org/wmt17/translation-task/news.2016.tr.shuffled.gz).
  - The sentences are translated into EN with a single TR->EN NMT system (~14 BLEU on newstest2016).
  - Turkish side is tokenized with a [slightly modified version](scripts/tokenizerv2.perl) of Moses tokenizer
    which handles apostrophes correctly for Turkish.
