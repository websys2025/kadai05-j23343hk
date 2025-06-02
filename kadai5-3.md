## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能
・エンドポイント：https://zipcloud.ibsnet.co.jp/api/search
・機能　　　　　：指定された郵便番号からの住所情報取得
* リクエストとレスポンスのフォーマット
・リクエスト：const aRes = await fetch(`${endpoint}?zipcode=${myForm.zipcode.value}`);
・レスポンス：例(2900024)
            { "message": null, "results": [ { "address1": "千葉県", "address2": "市原市", "address3": "根田", "kana1": "ﾁﾊﾞｹﾝ", "kana2": "ｲﾁﾊﾗｼ", "kana3": "ﾈﾀﾞ", "prefcode": "12", "zipcode": "2900024" } ], "status": 200 }

### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL
・API：REST Countries API
・URL：https://restcountries.com/
* エンドポイントと機能
・エンドポイント：https://restcountries.com/v3.1/all?fields=name,capital
・機能　　　　　：指定された国名からの首都名取得
* リクエストとレスポンスのフォーマット
・リクエスト：const endpoint = "https://restcountries.com/v3.1/all?fields=name,capital";
　　　　　　　const aRes = await fetch(endpoint);
・レスポンス：例(Japan)
            Japan : Tokyo
### Q3-3. 感想
* 今回の課題で苦労したこと
    初めてのWebAPIの読み取り操作
* 演習を通して理解できたこと
    APIからのデータ取得及び表示
* Web APIの利便性や課題など
    必要データの表示が比較的容易であるが、データ構造の理解が必要であること
