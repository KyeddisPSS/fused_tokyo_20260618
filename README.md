# Fused.io ハンズオン セッション
 
## 🚀 セッション開始はこちら
 
| リンク | 説明 |
|--------|------|
| [Fused.io アプリを開く](https://app.fused.io) | セッション用クラウド環境 |
| [ハンズオン ノートブック](#) | 本日使用するノートブック |
| [サンプルデータ](#) | セッション用データセット |
 
---
 
Fused.io はクラウドベースの Python データ分析・処理プラットフォームです。  
本セッションでは、実際に手を動かしながら基本的な使い方を学びます。
 
---
 
## 🔗 便利なリンク集

### はじめに
| リンク | 説明 |
|--------|------|
| [Fused.io 公式サイト](https://www.fused.io) | トップページ |
| [アカウント登録](https://www.fused.io/api/auth/login?returnTo=%2Fworkbench) | 無料アカウントの作成 |

### ドキュメント
| リンク | 説明 |
|--------|------|
| [公式ドキュメント](https://docs.fused.io) | 全体リファレンス |
| [クイックスタート](https://docs.fused.io/guide/guide-overview) | 最初の一歩 |
| [Python SDK リファレンス](https://docs.fused.io/python-sdk) | API 詳細 |

---

## 💻 ローカル環境セットアップ

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
