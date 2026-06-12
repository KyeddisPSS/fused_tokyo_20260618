# Fused.io ハンズオン セッション

Fused.io はクラウドベースの Python データ分析・処理プラットフォームです。  
本セッションでは、実際に手を動かしながら基本的な使い方を学びます。

---

## 🔗 便利なリンク集

### はじめに
| リンク | 説明 |
|--------|------|
| [Fused.io 公式サイト](https://www.fused.io) | トップページ |
| [Fused.io アプリ](https://app.fused.io) | クラウド環境へのログイン |
| [アカウント登録](https://app.fused.io/signup) | 無料アカウントの作成 |

### ドキュメント
| リンク | 説明 |
|--------|------|
| [公式ドキュメント](https://docs.fused.io) | 全体リファレンス |
| [クイックスタート](https://docs.fused.io/quickstart) | 最初の一歩 |
| [Python SDK リファレンス](https://docs.fused.io/python-sdk) | API 詳細 |

### 学習リソース
| リンク | 説明 |
|--------|------|
| [サンプル集 (GitHub)](https://github.com/fusedio/udfs) | 公式サンプル UDF |
| [チュートリアル](https://docs.fused.io/tutorials) | ステップバイステップガイド |
| [コミュニティ Discord](https://discord.gg/BxS5wMzdRk) | 質問・情報共有 |

---

## 🛠️ セッション前の準備

```bash
# Python SDK のインストール
pip install fused
```

```python
import fused

# 動作確認
import fused

# UDFの作成
@fused.udf()
def my_udf():
    import pandas as pd
    return pd.DataFrame({'hello': ['world']})

df = fused.run(my_udf)
print(df)

dc_file_udf = fused.load('https://github.com/fusedio/udfs/tree/main/public/DC_File_Example')

df2 = fused.run(dc_file_udf)
print(df2)
```

---

## 📝 メモ
