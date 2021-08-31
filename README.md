# Getting Started with Ruby

Ruby adalah bahasa pemrograman dinamis berbasis skrip yang berorientasi objek. Tujuan dari ruby adalah menggabungkan kelebihan dari semua bahasa-bahasa pemrograman skrip yang ada di dunia. Ruby ditulis dengan bahasa pemrograman C dengan kemampuan dasar seperti Perl dan Python.

Contoh aplikasi yang menggunakan bahasa pemrograman Ruby :

1. Twitter
2. Urban Dictionary
3. Shopify
4. Github
5. Basecamp

## Ruby Syntax and Strings

> Gunakan `puts` untuk mencetak baris. Dan gunakan `#` untuk membuat komentar.

```ruby
puts "Hello I'm Ruby!"
puts 'Hello World!'
# puts "This is comment"
```

```console
Hello I'm Ruby!
Hello World!
```

### Integers and Basic Calculations

> Untuk mencetak baris tidak diperlukan `"` atau `'`.

```ruby
puts 2
puts 2 + 3
puts 7 - 4
puts 3 * 5
puts 6 / 2
puts 9 % 2
```

```console
2
5
3
15
3
1
```

### String Concatenation

> Digunakan untuk menggabungkan 2 atau lebih _Strings_.

```ruby
puts "Hello " + "Ruby"
puts "3" + "5"
puts 3 + 5
```

```console
Hello Ruby
35
8
```

## Variable

> Digunakan untuk menyimpan nilai. Dan contoh penggunaan dari Variabel adalah : `date`, `user_name`.

```ruby
name = "John"
puts name
greeting = "Hello, selamat siang "
puts greeting + name

puts "----------"

number1 = 10
number2 = 5
puts number1 + number 2

puts "----------"

number = 2
puts number
number = number + 3
puts number
```

```console
John
Hello, selamat siang John
----------
15
----------
2
5
```

### String Interpolation

> Digunakan untuk menyisipkan variabel ke dalam sebuah _strings_.

```ruby
name = "Lerian"
puts "Hello, #{name}."
```

```console
Hello, Lerian.
```

## Booleans and Conditions

> Penggunakan logika, logika if dan juga `true` or `false`.

```ruby
score = 94
if score > 80
    puts "Great job!"
end

if score < 2
    puts "Benar!"
end

puts score > 80
puts score < 80
```

```console
Great job!
# ini kosong
true
false
```

### Comparison Operator

> Menggunakan: `<` `<=` `>` `>=` `==` `!=`

```ruby
score = 70
puts score == 100       ... false
puts score != 100       ... true
name = "John"
puts name == "John"       ... true
puts name != "John"       ... false
```

### else Statements

> Digunakan jika nilainya ada yang _false_.

```ruby
score = 100
if score == 100
    puts "Great job!"
else
    puts "You can do better!"
end
```

```console
Great Job!
```

### elsif Statements

> Digunakan jika ada lebih dari 2 kondisi _false_.

```ruby
score = 77
if score > 80
    puts "Great job!"
elsif score > 60
    puts "Not bad!"
else
    puts "You can do better!"
end
```

```console
Not bad!
```

### Combining Conditions

> Dengan cara menggunakan `&& (AND)` atau `|| (OR)`.

![](/img/and.png) ![](/img/and2.png)
![](/img/or.png) ![](/img/or.png)

```ruby
score = 68
if score <= 80 && score > 60
    puts "Not bad!"
end
```

```console
Not bad!
```
