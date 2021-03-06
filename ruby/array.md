# Array 関連問題

- [1, 2, 3, 4, 5] とeachメソッドを使用して、
  <br>[2, 4, 6, 8, 10]を作成するコードを記述してください。

  <details>
    <summary>ヒント</summary>

    ```
    # [1, 2, 3, 4, 5]から[10, 20, 30, 40, 50]を作成
    result = []
    [1, 2, 3, 4, 5].each do |i|
      result << i * 10
    end
    ```

  </details>

  <details>
    <summary>解答</summary>

    ```
    # [1, 2, 3, 4, 5]から[2, 4, 6, 8, 10]を作成
    result = []
    [1, 2, 3, 4, 5].each do |i|
      result << i * 2
    end
    ```

  </details>

- [1, 2, 3, 4, 5] とmapメソッドを使用して、
  <br>[2, 4, 6, 8, 10]を作成するコードを記述してください。

  <details>
    <summary>ヒント</summary>

    ```
    # [1, 2, 3, 4, 5]から[10, 20, 30, 40, 50]を作成
    result = [1, 2, 3, 4, 5].map do |i|
      i * 10
    end
    ```

  </details>

  <details>
    <summary>解答</summary>

    ```
    # [1, 2, 3, 4, 5]から[2, 4, 6, 8, 10]を作成
    result = [1, 2, 3, 4, 5].map do |i|
      i * 2
    end
    ```

  </details>

- [1, 2, 3, 4, 5] とmap!メソッドを使用して、
  <br>[2, 4, 6, 8, 10]を作成するコードを記述してください。

  <details>
    <summary>ヒント</summary>

    ```
    # [1, 2, 3, 4, 5]から[10, 20, 30, 40, 50]を作成
    result = [1, 2, 3, 4, 5]
    result.map! do |i|
      i * 10
    end
    ```

  </details>

  <details>
    <summary>解答</summary>

    ```
    # [1, 2, 3, 4, 5]から[2, 4, 6, 8, 10]を作成
    result = [1, 2, 3, 4, 5]
    result.map! do |i|
      i * 2
    end
    ```

  </details>

- 以下のコードの①～③にeach, map, map! を記入して、コードを完成させてください。
  <br>なお、同じメソッドを複数回記入してもかまいませんし、使用しないメソッドがあっても構いません
  ```rb
  require 'bigdecimal'

  base_prices = [100, 200, 300]
  TAX_RATE    = 1.08

  # 税抜き価格をそれぞれ50円値上げ
  base_prices.① do |base_price|
    base_price + 50
  end

  # 税込み価格の計算
  # 参考： https://qiita.com/jnchito/items/d0ef71b25732ad5a881c
  tax_include_prices = base_prices.② do |base_price|
    (BigDecimal(base_price.to_s) * BigDecimal(TAX_RATE.to_s)).round
  end

  # 税込み価格の表示
  tax_include_prices.③ do |tax_include_price|
    puts tax_include_price
  end

  =>162
    270
    378
  ```

  <details>
    <summary>ヒント</summary>

    なし

  </details>

  <details>
    <summary>解答</summary>

    - ①: map!
    - ②: map
    - ③: each

  </details>

