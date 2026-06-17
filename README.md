<img src="https://miro.medium.com/v2/resize:fit:1400/1*0Ky8lQUvhozFSDJgQXpw-w.png" width="800"/>

# Fused.io ハンズオン セッション
 
## 🚀 セッション開始はこちら
 
| リンク | 説明 |
|--------|------|
| [キャンバス例１](https://www.fused.io/canvas/fc_2iT7Nl69JiwcOzKkIKIa2N) | ジオ展交通事故キャンバス |
| [キャンバス例２](https://www.fused.io/canvas/fc_7aeTlOg2S9UwBO4MJASK86) | ジオ展地震影響キャンバス |
| [ハンズオン1](https://www.fused.io/canvas/fc_3iIG5erQJf0JjuFUhTCxjy) | ハンズオンの未完成キャンバス |
| [ハンズオン2](https://www.fused.io/canvas/fc_53COHnUmDWUhxCFbC3SRlg) | ハンズオンの完成キャンバス |
| [ハンズオン3](https://www.fused.io/canvas/fc_3EwyXkpLPCggIlfrtMdUvc) | ハンズオンのボーナスキャンバス |
 
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
