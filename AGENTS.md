# エージェント向け作業ルール

## リポジトリの目的

このリポジトリは、以前 OSS として開発していた Kamo から独立させた研究用リポジトリです。研究のために自由に実装・実験を行う場であり、元の OSS や upstream への変更反映を目的としません。

## 変更対象とリモートの制約

- このファイルのルールは、`third_party` を含むリポジトリ全体の作業に適用します。
- 親リポジトリの変更先は、`origin` の [wasanemon/Kamo-research](https://github.com/wasanemon/Kamo-research) のみに限定します。
- `upstream` には決して触れないでください。push、fetch、pull、PR 作成、リモート設定の変更など、`upstream` に対する操作は禁止です。URL を直接指定するなど、別の方法で元の OSS にアクセス・変更することも禁止です。
- `third_party/LineairDB` も同様に、変更先はその `origin` の [wasanemon/LineairDB-research](https://github.com/wasanemon/LineairDB-research) のみに限定します。LineairDB の元リポジトリや `upstream` には触れないでください。
- リモート操作の前に、ローカルの設定で対象 URL を確認してください。`origin` が上記の研究用リポジトリを指していない場合は、操作を止めてユーザーに確認してください。
- `--all` や `--mirror` など、許可されていないリモートや対象に影響し得る一括操作は行わないでください。

## commit・push とユーザーへの確認

- ユーザーの明示的な承認なしに、勝手に `git commit` や `git push` を実行しないでください。
- commit・push を行う際は、対象リポジトリ、変更内容、対象ブランチ、push 先を該当する範囲で提示し、実行前にユーザーへ確認を求めてください。commit の承認だけで push も承認されたと解釈しないでください。
- この確認ルールは、親リポジトリと `third_party/LineairDB` を含むサブモジュールの両方に適用します。
- 実装・修正の依頼を、commit・push の承認と解釈しないでください。依頼されたローカルの編集・検証を進め、結果を提示してから確認してください。
- 操作対象や許可範囲に迷う場合は、推測で実行せずユーザーに確認してください。
