# コントリビューションガイド

OraDB DUMP Viewer へのコントリビューションに興味をお持ちいただきありがとうございます。

---

## はじめに

### CLA (コントリビューターライセンス同意書)

Pull Request を提出する前に、[CLA](https://github.com/OraDB-DUMP-Viewer/OraDB-DUMP-Viewer/blob/main/CLA.md) への署名が必要です。
PR を提出すると、CLA Assistant が自動的に署名を求めます。

### ソースコードの取り扱い

本リポジトリのソースコードは **参照目的** で公開されています。

| 利用形態 | 可否 |
|---|---|
| ソースコードの閲覧・学習 | **可** |
| Pull Request による貢献 | **可** (CLA 署名が必要) |
| 改変して再配布 | **不可** |
| 類似の商用製品の作成 | **不可** |

---

## 開発環境のセットアップ

### 必要なツール

| ツール | バージョン |
|---|---|
| Visual Studio | 2026 (MSVC C++ ツールチェーン含む) |
| .NET SDK | 10.0 |

### ビルド手順

```bash
# 1. リポジトリのクローン
git clone https://github.com/OraDB-DUMP-Viewer/OraDB-DUMP-Viewer.git
cd OraDB-DUMP-Viewer

# 2. C ネイティブ DLL のビルド
cd Logics/DumpParser
_build.cmd

# 3. VB.NET アプリケーションのビルド
cd ../..
dotnet build "OraDB DUMP Viewer.vbproj"
```

---

## コーディング規約

### VB.NET

- クラス・メソッド: **PascalCase**
- プライベートフィールド: **_camelCase**
- ローカル変数: **camelCase**
- `#Region` / `#End Region` でコードをグループ化
- XML Documentation (`'''`) を public メソッドに記述
- UI 定義は `*.Designer.vb` に完全隔離

### C

- 関数名: `odv_` プレフィクス (例: `odv_open_session`)
- 型名: `ODV_` プレフィクス (例: `ODV_SESSION`)
- 定数: `ODV_` プレフィクス + 大文字 (例: `ODV_OK`)
- C11 標準準拠

---

## Pull Request の手順

1. リポジトリをフォーク
2. 機能ブランチを作成 (`git checkout -b feature/my-feature`)
3. 変更をコミット
4. フォークにプッシュ (`git push origin feature/my-feature`)
5. Pull Request を作成
6. CLA に署名

### PR のガイドライン

- 1 つの PR では 1 つの変更に集中してください
- PR テンプレートに沿って記述してください
- 既存のコーディング規約に従ってください

---

## Issue の報告

- **バグ報告**: [Bug Report テンプレート](https://github.com/OraDB-DUMP-Viewer/OraDB-DUMP-Viewer/issues/new?template=bug_report.yml) を使用
- **機能リクエスト**: [Feature Request テンプレート](https://github.com/OraDB-DUMP-Viewer/OraDB-DUMP-Viewer/issues/new?template=feature_request.yml) を使用
- **セキュリティ脆弱性**: Issue ではなく [inquiry@ta-yan.ai](mailto:inquiry@ta-yan.ai) にメールで報告

---

## お問い合わせ

- **一般的な質問**: [GitHub Issues](https://github.com/OraDB-DUMP-Viewer/OraDB-DUMP-Viewer/issues)
- **セキュリティ報告**: [inquiry@ta-yan.ai](mailto:inquiry@ta-yan.ai)
- **ライセンス**: [https://www.odv.dev/](https://www.odv.dev/)

---

<p align="center">
  <strong>YANAI Taketo</strong><br>
  <a href="https://www.odv.dev/">https://www.odv.dev/</a>
</p>
