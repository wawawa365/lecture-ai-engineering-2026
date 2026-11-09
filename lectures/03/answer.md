# 第3回 解答

## 演習

- 第1回（素のLLM）とエージェントの回答の違い：しっかり正しい定義を答えるようになった
- `--trace` で見えたツール呼び出し（ツール名と引数）：[tool call]   search_glossary({'query': 'LoRA'})
[tool call]   search_glossary({'query': 'QLoRA'})
[tool return] search_glossary -> [{"term": "LoRA", "lecture": 2, "definition":
- 1つの質問での LLM 呼び出し回数（`requests`）：2
- 追加したツールと、docstring に書いた説明：追加したツール　make_quiz 
説明　指定した回の用語から 1つを選び、
確認問題と答えを返す。
「第2回の確認問題を出して」のように、
復習用の問題を求められたときに使う

## 宿題

- 取り組んだレベル：基礎
- やったこと：search_glossaryのdocstringを変更。docstring の「用語を1つだけ入れる」を「まとめて入れる」に変える
- 結果：引数がまとめて検索されるようになった
- 気づき・疑問：まとめて検索されるようになったが、rerturnは一つの用語に関するものだけになっている気がする。しかし返答はしっかり答えられているのが疑問だった。
