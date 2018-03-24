# ActiveRecord 関連問題

## 使用するモデル

- 社員(Employee)

  |論理名  |物理名    |データ型|
  |--------|----------|--------|
  |ID(PK)  |id        |Int     |
  |社員番号|number    |VARCHAR |
  |名前    |full_name |VARCHAR |
  |ふりがな|kana_name |VARCHAR |
  |入社日  |joined_day|Date    |

## 問題

- selectメソッドを使用して、全社員の「社員番号」及び「名前」を
  <br>取得するコードを記述してください。

- pluckメソッドを使用して、全社員の「ふりがな」を取得するコードを記述してください。

- 以下の①～④を記述して、コードを完成させてください。

  ```rb
  # 2010/04/01以前に入社の社員名を表示
  long_employee_names = Employee.where('joined_day <= ?', Date.new(2010, 4, 1)).①
  long_employee_names.each do |name|
    puts ②
  end

  # 2010/04/01よりも後に入社の社員名を社員番号付きで表示
  short_employees = Employee.where('joined_day > ?', Date.new(2010, 4, 1)).③
  short_employees.each do |employee|
    # "#{社員番号}: #{社員名}"の形で表示
    puts ④
  end
  ```

