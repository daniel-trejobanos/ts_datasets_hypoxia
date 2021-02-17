<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="wmt16_translate" />
  <meta itemprop="description" content="Translate dataset based on the data from statmt.org.&#10;&#10;Versions exists for the different years using a combination of multiple data&#10;sources. The base `wmt_translate` allows you to create your own config to choose&#10;your own data/language pair by creating a custom `tfds.translate.wmt.WmtConfig`.&#10;&#10;```&#10;config = tfds.translate.wmt.WmtConfig(&#10;    version=&quot;0.0.1&quot;,&#10;    language_pair=(&quot;fr&quot;, &quot;de&quot;),&#10;    subsets={&#10;        tfds.Split.TRAIN: [&quot;commoncrawl_frde&quot;],&#10;        tfds.Split.VALIDATION: [&quot;euelections_dev2019&quot;],&#10;    },&#10;)&#10;builder = tfds.builder(&quot;wmt_translate&quot;, config=config)&#10;```&#10;&#10;&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;wmt16_translate&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/wmt16_translate" />
  <meta itemprop="sameAs" content="http://www.statmt.org/wmt16/translation-task.html" />
  <meta itemprop="citation" content="&#10;@InProceedings{bojar-EtAl:2016:WMT1,&#10;  author    = {Bojar, Ond{r}ej  and  Chatterjee, Rajen  and  Federmann, Christian  and  Graham, Yvette  and  Haddow, Barry  and  Huck, Matthias  and  Jimeno Yepes, Antonio  and  Koehn, Philipp  and  Logacheva, Varvara  and  Monz, Christof  and  Negri, Matteo  and  Neveol, Aurelie  and  Neves, Mariana  and  Popel, Martin  and  Post, Matt  and  Rubino, Raphael  and  Scarton, Carolina  and  Specia, Lucia  and  Turchi, Marco  and  Verspoor, Karin  and  Zampieri, Marcos},&#10;  title     = {Findings of the 2016 Conference on Machine Translation},&#10;  booktitle = {Proceedings of the First Conference on Machine Translation},&#10;  month     = {August},&#10;  year      = {2016},&#10;  address   = {Berlin, Germany},&#10;  publisher = {Association for Computational Linguistics},&#10;  pages     = {131--198},&#10;  url       = {http://www.aclweb.org/anthology/W/W16/W16-2301}&#10;}&#10;" />
</div>
# `wmt16_translate`

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
    [http://www.statmt.org/wmt16/translation-task.html](http://www.statmt.org/wmt16/translation-task.html)
*   **Source code**:
    [`tfds.translate.wmt16.Wmt16Translate`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/translate/wmt16.py)
*   **Versions**:
    *   **`1.0.0`** (default): No release notes.
    *   `0.0.3`: No release notes.
*   **Download size**: `1.57 GiB`
*   **Dataset size**: `Unknown size`
*   **Manual download instructions**: This dataset requires you to download the
    source data manually into `download_config.manual_dir`
    (defaults to `~/tensorflow_datasets/manual/wmt16_translate/`):<br/>
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
@InProceedings{bojar-EtAl:2016:WMT1,
  author    = {Bojar, Ond{r}ej  and  Chatterjee, Rajen  and  Federmann, Christian  and  Graham, Yvette  and  Haddow, Barry  and  Huck, Matthias  and  Jimeno Yepes, Antonio  and  Koehn, Philipp  and  Logacheva, Varvara  and  Monz, Christof  and  Negri, Matteo  and  Neveol, Aurelie  and  Neves, Mariana  and  Popel, Martin  and  Post, Matt  and  Rubino, Raphael  and  Scarton, Carolina  and  Specia, Lucia  and  Turchi, Marco  and  Verspoor, Karin  and  Zampieri, Marcos},
  title     = {Findings of the 2016 Conference on Machine Translation},
  booktitle = {Proceedings of the First Conference on Machine Translation},
  month     = {August},
  year      = {2016},
  address   = {Berlin, Germany},
  publisher = {Association for Computational Linguistics},
  pages     = {131--198},
  url       = {http://www.aclweb.org/anthology/W/W16/W16-2301}
}
```

## wmt16_translate/cs-en (default config)

*   **Config description**: WMT 2016 cs-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | ---------:
'test'       | 2,999
'train'      | 52,335,651
'validation' | 2,656

## wmt16_translate/de-en

*   **Config description**: WMT 2016 de-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | --------:
'test'       | 2,999
'train'      | 4,548,885
'validation' | 2,169

## wmt16_translate/fi-en

*   **Config description**: WMT 2016 fi-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | --------:
'test'       | 6,000
'train'      | 2,073,394
'validation' | 1,370

## wmt16_translate/ro-en

*   **Config description**: WMT 2016 ro-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | -------:
'test'       | 1,999
'train'      | 610,320
'validation' | 1,999

## wmt16_translate/ru-en

*   **Config description**: WMT 2016 ru-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | --------:
'test'       | 2,998
'train'      | 2,516,162
'validation' | 2,818

## wmt16_translate/tr-en

*   **Config description**: WMT 2016 tr-en translation task dataset.
*   **Splits**:

Split        | Examples
:----------- | -------:
'test'       | 3,000
'train'      | 205,756
'validation' | 1,001