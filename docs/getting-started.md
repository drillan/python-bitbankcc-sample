---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# はじめてみよう

## インストール

ここでは、 [bitbank, inc. （ビットバンク株式会社）公式のPythonクライアント](https://github.com/bitbankinc/python-bitbankcc) をインストールします。

{numref}`install-python-client` のコマンドを実行します。

```{code-block} bash
:name: install-python-client
:caption: Pythonクライアントのインストール

pip install requests git+https://github.com/bitbankinc/python-bitbankcc
```

## パブリックAPIの利用

`public` クラスは、パブリックAPIを利用するためのクラスです。

```{code-cell} ipython3
import python_bitbankcc

public = python_bitbankcc.public()
```

`get_ticker` メソッドは、引数に指定したペアの次の値を辞書で返します。

sell
: 売気配

buy
: 買気配

open
: 始値

high
: 高値

low
: 安値

last
: 終値

vol
: 出来高

timestamp
: タイムスタンプ

```{code-cell} ipython3
public.get_ticker("btc_jpy")
```