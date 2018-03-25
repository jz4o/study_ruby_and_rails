# Date 関連問題

- '2000年1月1日'を元に、Dateオブジェクトを作成するコードを記述してください。

  <details>
    <summary>ヒント</summary>

    ```
    # '2000,01,01'からDateオブジェクトを作成
    result = Date.strptime '2000,01,01', '%Y,%m,%d'
    ```

  </details>

  <details>
    <summary>解答</summary>

    ```
    # '2000年1月1日'からDateオブジェクトを作成
    result = Date.strptime '2000年1月1日', '%Y年%m月%d日'
    ```

  </details>

- 2000年1月1日のDateオブジェクトを元に、
  <br>"2000年1月1日"を作成するコードを記述してください。

  <details>
    <summary>ヒント</summary>

    ```
    # 2000年1月1日のDateオブジェクト
    date = Date.new(2000, 1, 1)

    # "2000, 1, 1" を作成
    result = date.strftime '%Y,%_m,%_d'
    ```

  </details>

  <details>
    <summary>解答</summary>

    ```
    # 2000年1月1日のDateオブジェクト
    date = Date.new(2000, 1, 1)

    # "2000年1月1日"を作成
    result = date.strftime '%Y年%-m月%-d日'
    ```

  </details>

- 2000年1月1日のDateオブジェクトを元に、
  <br>"2000-01-01"を作成するコードを記述してください。
  <br>ただし、strftimeメソッドは使用しないでください。
  <br>なお、"2000-01-01"は、ISO8601で定められた年月日の表記形式(拡張形式)です。

  <details>
    <summary>ヒント</summary>

    ```
    # 2000年1月1日のDateオブジェクト
    date = Date.new(2000, 1, 1)

    # "H12.01.01"（JIS X 0301で定められた表記形式）を作成
    result = date.jisx0301
    ```

  </details>

  <details>
    <summary>解答</summary>

    ```
    # 2000年1月1日のDateオブジェクト
    date = Date.new(2000, 1, 1)

    # "2000-01-01"を作成
    result = date.iso8601
    ```

  </details>

