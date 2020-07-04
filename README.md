# LearnBayesNN
ベイズ深層学習の自学コード

## 確率分布
tfp では、 [`tfp.distributions`](https://www.tensorflow.org/probability/api_docs/python/tfp/distributions) の中に、様々な基本的な確率分布を表現するクラスが実装されている



## 同時確率
tfpでは、`JointDistribution` を継承した3つのクラスを利用する実装方法がある。

* `JointDistributionSequence`
  * keras の `Sequence` のように配列で実装する
  * 注意点は、逆順に引数に渡されること。
* `JointDistributionNamed`
  * `dict` として、変数と分布をペアにして設定する
* `JointDistributionCoroutine`
  * コルーチンの `yield` を利用して実装する


## 参照
* D. Piponi _et al_., "Joint Distributions for TensorFlow Probability",arXiv cs.PL 2001.11819 (2020) https://arxiv.org/abs/2001.11819
