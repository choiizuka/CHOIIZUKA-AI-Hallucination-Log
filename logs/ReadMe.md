このディレクトリへPDFファイルをプッシュすると自動的に改ざん不能なログが生成可能

---
# CHOIIZUKA-AI-Hallucination-Log
CHOIIZUKA-AI Hallucination Log ー AIハルシネーションログ

## Google/Microsoft社などAIの誤出力による名誉毀損問題改竄防止ログ保存システム

### 推奨ワークフロー概要
1. **PDFを `logs/` に push**  
2. **GitHub Actions がトリガー**（`paths: logs/**/*.pdf`）  
3. **Actions内で SHA256 を算出**し、メタ情報（日時・ファイル名・クエリ等）を YAML/JSONL に追加または新規作成  
4. **GITHUB_TOKEN で自動コミット**（ハッシュ付きの index ファイルを更新）  
5. **（任意）TSA でタイムスタンプ取得 or ブロックチェーン刻印** を並行実行して補強  
6. **公開版は個人情報をマスクした要約、原本は非公開ストレージに保管**

---
(C)2026 CHOIIZUKA.COM
