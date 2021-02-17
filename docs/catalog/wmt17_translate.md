<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="wmt17_translate" />
  <meta itemprop="description" content="Translate dataset based on the data from statmt.org.&#10;&#10;Versions exists for the different years using a combination of multiple data&#10;sources. The base `wmt_translate` allows you to create your own config to choose&#10;your own data/language pair by creating a custom `tfds.translate.wmt.WmtConfig`.&#10;&#10;```&#10;config = tfds.translate.wmt.WmtConfig(&#10;    version=&quot;0.0.1&quot;,&#10;    language_pair=(&quot;fr&quot;, &quot;de&quot;),&#10;    subsets={&#10;        tfds.Split.TRAIN: [&quot;commoncrawl_frde&quot;],&#10;        tfds.Split.VALIDATION: [&quot;euelections_dev2019&quot;],&#10;    },&#10;)&#10;builder = tfds.builder(&quot;wmt_translate&quot;, config=config)&#10;```&#10;&#10;&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;wmt17_translate&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/wmt17_translate" />
  <meta itemprop="sameAs" content="http://www.statmt.org/wmt17/translation-task.html" />
  <meta itemprop="citation" content="&#10;@InProceedings{bojar-EtAl:2017:WMT1,&#10;  author    = {Bojar, Ond{r}ej  and  Chatterjee, Rajen  and  Federmann, Christian  and  Graham, Yvette  and  Haddow, Barry  and  Huang, Shujian  and  Huck, Matthias  and  Koehn, Philipp  and  Liu, Qun  and  Logacheva, Varvara  and  Monz, Christof  and  Negri, Matteo  and  Post, Matt  and  Rubino, Raphael  and  Specia, Lucia  and  Turchi, Marco},&#10;  title     = {Findings of the 2017 Conference on Machine Translation (WMT17)},&#10;  booktitle = {Proceedings of the Second Conference on Machine Translation, Volume 2: Shared Task Papers},&#10;  month     = {September},&#10;  year      = {2017},&#10;  address   = {Copenhagen, Denmark},&#10;  publisher = {Association for Computational Linguistics},&#10;  pages     = {169--214},&#10;  url       = {http://www.aclweb.org/anthology/W17-4717}&#10;}&#10;" />
</div>
# `wmt17_translate`

Warning: Manual download required. See instructions bellow.

*   **Description**:

Translate dataset based on the data from statmt.org.

Versions exists for the different years using a combination of multiple data
sources. The base `wmt_translate` allows you to create your own config to choose
your own data/language pair by creating a custom `tfds.translate.wmt.WmtConfig`.

```
config = tfds.translate.wmt.WmtConfig(
    version="0.0.1",
    language_pair=("fr", "de"),
    subsets={
        tfds.Split.TRAIN: ["commoncrawl_frde"],
        tfds.Split.VALIDATION: ["euelections_dev2019"],
    },
)
builder = tfds.builder("wmt_translate", config=config)
```

*   **Homepage**:
    [http://www.statmt.org/wmt17/translation-task.html](http://www.statmt.org/wmt17/translation-task.html)
*   **Source code**:
    [`tfds.translate.wmt17.Wmt17Translate`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/translate/wmt17.py)
*   **Versions**:
    *   **`1.0.0`** (default): No release notes.
    *   `0.0.3`: No release notes.
*   **Download size**: `1.66 GiB`
*   **Dataset size**: `Unknown size`
*   **Manual download instructions**: This dataset requires you to download the
    source data manually into `download_config.manual_dir`
    (defaults to `~/tensorflow_datasets/manual/wmt17_translate/`):<br/>
    Some of the wmt configs here, require a manual download.
    Please look into wmt.py to see the exact path (and file name) that has to
    be downloaded.
*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    No
*   **Features**:

```python
Translation({
    'cs': Text(shape=(), dtype=tf.string),
    'en': Text(shape=(), dtype=tf.string),
})
```
*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load)):
    `('cs', 'en')`
*   **Citation**:

```
@InProceedings{bojar-EtAl:2017:WMT1,
  author    = {Bojar, Ond{r}ej  and  Chatterjee, Rajen  and  Federmann, Christian  and  Graham, Yvette  and  Haddow, Barry  and  Huang, Shujian  and  Huck, Matthias  and  Koehn, Philipp  and  Liu, Qun  and  Logacheva, Varvara  and  Monz, Christof  and  Negri, Matteo  and  Post, Matt  and  Rubino, Raphael  and  Specia, Lucia  and  Turchi, Marco},
  title     = {Findings of the 2017 Conference on Machine Translation (WMT17)},
  booktitle = {Proceedings of the Second Conference on Machine Translation, Volume 2: Shared Task Papers},
  month     = {September},
  year      = {2017},
  address   = {Copenhagen, Denmark},
  publisher = {Association for Computational Linguistics},
  pages     = {169--214},
  url       = {http://www.aclweb.org/anthology/W17-4717}
}
```

## wmt17_translate/cs-en (default config)

*   **Config description**: WMT 2017 cs-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | ---------:
'test'       | 3,005
'train'      | 15,851,649
'validation' | 2,999

## wmt17_translate/de-en

*   **Config description**: WMT 2017 de-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | --------:
'test'       | 3,004
'train'      | 5,906,184
'validation' | 2,999

## wmt17_translate/fi-en

*   **Config description**: WMT 2017 fi-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | --------:
'test'       | 6,004
'train'      | 2,656,542
'validation' | 6,000

## wmt17_translate/lv-en

*   **Config description**: WMT 2017 lv-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | --------:
'test'       | 2,001
'train'      | 3,567,528
'validation' | 2,003

## wmt17_translate/ru-en

*   **Config description**: WMT 2017 ru-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | ---------:
'test'       | 3,001
'train'      | 25,782,720
'validation' | 2,998

## wmt17_translate/tr-en

*   **Config description**: WMT 2017 tr-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | -------:
'test'       | 3,007
'train'      | 205,756
'validation' | 3,000

## wmt17_translate/zh-en

*   **Config description**: WMT 2017 zh-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | ---------:
'test'       | 2,001
'train'      | 25,136,609
'validation' | 2,002