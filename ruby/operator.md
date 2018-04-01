# 演算子 関連問題

- 以下のコードと同等のコードを3項演算子を用いて記述してください。

  ```
  flag = true
  result = nil
  if flag
    result = 'ok'
  else
    result = 'ng'
  end
  ```

  <details>
    <summary>ヒント</summary>

    ```
    result = nil ? 'ok' : 'ng'
    # => 'ng'
    ```

  </details>

- ||演算子を用いて、resultがnilの場合、
  <br>'default_value'を代入してください。

  <details>
    <summary>ヒント</summary>

    ```
    result = 'ok' || 'ng'
    # => 'ok'

    result = false || 'ng'
    # => 'ng'

    # result = result || 'ok' は以下と書くこともできます
    result ||= 'ok'
    ```

  </details>

- &&演算子を用いて、resultがnil/falseではない場合、
  <br>末尾に'\_suffix'を追加してください。

  <details>
    <summary>ヒント</summary>

    ```
    result = 'ng' && 'ok'
    # => 'ok'

    result = nil && 'ok'
    # => nil

    # result = result && 'ok' は以下と書くこともできます
    result &&= 'ok'
    ```

  </details>

- 以下の①～④を記入して、コードを完成させてください

  ```
  require 'date'

  era_names = {
    'M' => '明治',
    'T' => '大正',
    'S' => '昭和',
    'H' => '平成'
  }.freeze

  # 1850年から50年ごとの元日の元号を表示
  years = [1850, 1900, 1950, 2000]
  years.each do |year|
    date = Date.new year
    jis_date = date.jisx0301

    # Date#jisx0301は、明治6年(1873年)より前の日付の場合、ISO8601で返す
    # 参考： https://docs.ruby-lang.org/ja/latest/method/Date/i/jisx0301.html
    era_code, era_year = year >= 1873 ① [jis_date[0], jis_date[1, 2]]

    era_name = era_names[era_code]
    puts "#{year}年元日の元号は#{ era_name ② '明治以前' }"
    puts "なお、#{ era_code ③ "#{era_name}#{era_year}年" ④ '年数は不明' }"
  end
  ```

  <details>
    <summary>ヒント</summary>

    なし

  </details>

