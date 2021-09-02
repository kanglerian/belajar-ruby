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

### if else Statements

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

## Arrays, Hashes and Loops

### Arrays

```ruby
names = ["Lerian","Faisal","Sopyan"]

puts names
```

```console
Lerian
Faisal
Sopyan
```
### Using Arrays

```ruby
# Print Lerian
names = ["Lerian","Faisal","Sopyan"]

puts "Hello, selamat pagi #{names[0]}"
```

### The each Method

```ruby
names = ["Lerian","Faisal","Sopyan"]

names.each do |name|
    puts "Hello, #{name}"
end
```

## Hashes and Symbols

### Hashes

```ruby
user = {"name" => "Lerian", "age" => 21}

puts user
```

```console
{"name" => "Lerian", "age" => 21}
```

### Using Hashes, update dan add

```ruby
user = {"name" => "Lerian", "age" => 21}

puts user["name"]
```

```console
Lerian
```

```ruby
user = {"name" => "Lerian", "age" => 21}
user["name"] = "Lerian Febriana"
puts user["name"]
```

```console
Lerian Febriana
```

```ruby
user = {"name" => "Lerian Febriana", "age" => 21}
user["gender"] = "Male"
puts user
```

```console
{"name" => "Lerian", "age" => 21, "gender" => "Male"}
```

```ruby
user = {:name => "Lerian", :age => 21}

puts user[:name]
```

```console
Lerian
```

```ruby
user = {name: "Lerian", age: 21}

puts user[:name]
```

```console
Lerian
```

### Using if with nil

```ruby
user = {name: "Lerian", age: 23}
if user[:age]
  puts "#{user[:name]} is #{user[:age]} years old!"
else
  puts "#{user[:name]}'s age is unknown"
end
```

```console
Lerian is 23 years old!
```

### Arrays with Hash

```ruby
users = [
    {name:"Lerian",age:23},
    {name:"Sopyan",age:22},
]

user = users[0]

puts user[:name]
```

```console
Lerian
```

```ruby
users = [
    {name:"Lerian",age:23},
    {name:"Sopyan",age:22},
]

users.each do |user|
    puts user[:name]
end
```

```console
Lerian
Sopyan
```

#### Final Project or Example!

```ruby
characters = [
    {name: "Lerian", age: 23},
    {name: "Kamaludin"},
    {name: "Sopyan", age: 22},
    {name: "Asep"},
]
border = "-----------------"

characters.each do |character|
    puts border
    puts "Hallo, nama saya #{character[:name]}"

    if character[:age]
        puts "Usia saya #{character[:age]}"
    else
        puts "Usia saya rahasia :p"
    end
end
```

```console
-----------------
Hallo, nama saya Lerian
Usia saya 23
-----------------
Hallo, nama saya Kamaludin
Usia saya rahasia :p
-----------------
Hallo, nama saya Sopyan
Usia saya 23
-----------------
Hallo, nama saya Asep
Usia saya rahasia :p
```