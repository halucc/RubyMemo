# RubyMemo
Study Ruby

# うるう年判定

#### 条件
- 4で割り切れる
- 100で割り切れたらうるう年ではない
- 但し、400で割り切れたらうるう年

つまり、1900年はうるう年ではなく、2000年はうるう年

```ruby
#うるう年判定

# for文
for year in 1900..2020 do

  # 変数 / 判定用
  year4 = (year % 4).zero? # 多言語のように「== 0」でも記述できるが、Rubyでは「.zero?」推奨
  year100no = (year % 100) != 0
  year400 = (year % 400).zero?

  # if - else / 判定処理
  if year400
    puts year
  elsif year4 && year100no
    puts year
  end

end
```
