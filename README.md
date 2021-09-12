# **Getting Started with Ruby**

Ruby adalah bahasa pemrograman dinamis berbasis skrip yang berorientasi objek. Tujuan dari ruby adalah menggabungkan kelebihan dari semua bahasa-bahasa pemrograman skrip yang ada di dunia. Ruby ditulis dengan bahasa pemrograman C dengan kemampuan dasar seperti Perl dan Python.

Contoh aplikasi yang menggunakan bahasa pemrograman Ruby :

1. Twitter
2. Urban Dictionary
3. Shopify
4. Github
5. Basecamp

## **A. Ruby Syntax and Strings**

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

### - Integers and Basic Calculations

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

### - String Concatenation

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

## **B. Variable**

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

### - String Interpolation

> Digunakan untuk menyisipkan variabel ke dalam sebuah _strings_.

```ruby
name = "Lerian"
puts "Hello, #{name}."
```

```console
Hello, Lerian.
```

## **C. Booleans and Conditions**

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

### - Comparison Operator

> Menggunakan: `<` `<=` `>` `>=` `==` `!=`

```ruby
score = 70
puts score == 100       ... false
puts score != 100       ... true
name = "John"
puts name == "John"       ... true
puts name != "John"       ... false
```

### - if else Statements

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

### - elsif Statements

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

### - Combining Conditions

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

## **D. Arrays, Hashes and Loops**

### - Arrays

```ruby
names = ["Lerian","Faisal","Sopyan"]

puts names
```

```console
Lerian
Faisal
Sopyan
```
### - Using Arrays

```ruby
# Print Lerian
names = ["Lerian","Faisal","Sopyan"]

puts "Hello, selamat pagi #{names[0]}"
```

### - The each Method

```ruby
names = ["Lerian","Faisal","Sopyan"]

names.each do |name|
    puts "Hello, #{name}"
end
```

## **E. Hashes and Symbols**

### - Hashes

```ruby
user = {"name" => "Lerian", "age" => 21}

puts user
```

```console
{"name" => "Lerian", "age" => 21}
```

### - Using Hashes, update dan add

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

### - Using if with nil

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

### - Arrays with Hash Elements

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

# **Final Project I**

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

## **D. Methods**

```ruby
def introduce
  puts "Hello"
  puts "My name is Lerian"
  puts "Nice to meet you!"
end

puts "----Self Intro----"
introduce
```

```console
----Self Intro----
Hello
My name is Lerian
Nice to meet you!
```

## **E. Parameters and Arguments**

```ruby
def introduce(name)
  puts "Hello"
  puts "My name is #{name}"
end

# Call the introduce method with your own name
introduce("Lerian")
introduce
```

```console
Hello
My name is Lerian
```

### - Multiple Parameters

```ruby
def print_info(item,price)
  puts "Welcome to Ninja Electronics!"
  puts "#{item}s are on sale today! Only $#{price} each!"
end

print_info("Flash Drive",12)
```

```console
Welcome to Ninja Electronics!
Flash Drives are on sale today! Only $12 each!
```

## **F. Return Values**

```ruby
def discount(price)
  return price / 2
end

puts "Headphones are on sale today!"

half_price = discount(150)

puts "The sale price is $#{half_price}"
```

```console
Headphones are on sale today!
The sale price is $75
```

### - Tipes of Boolean Return

```ruby
def shipping_free?(price)
  return price >= 50
end

if shipping_free?(30)
  puts "Shipping is free for purchases above $50"
else
  puts "The shipping fee will be $5"
end
```

```console
The shipping fee will be $5
```

### - Multiple Return Values

```ruby
def price_with_shipping(price)
  if price >= 50
    return price
  end
	return price + 5
end

puts "The total price is $30"
puts "With shipping, it will be $#{price_with_shipping(30)}"
puts "-----------"
puts "The total price is $100"
puts "With shipping, it will be $#{price_with_shipping(100)}"
```

```console
The total price is $30
With shipping, it will be $35
-----------
The total price is $100
With shipping, it will be $100
```

## **G. Keyword Arguments**

```ruby
def buy(item:, price:, count:)
  puts "You have bought #{count} #{item}s"
  puts "The total price is $#{price * count}"
end
buy(item: "headphone", price: 150, count: 2)
```

```console
You have bought 2 headphones
The total price is $300
```

## **I. Classes and Instances**

### - Defining Class

```ruby
class Menu

end
```

### - Instances Variables

```ruby
class Menu
  attr_accessor :name
  attr_accessor :price
end
```

### - Creating an Instance

```ruby
class Menu
  attr_accessor :name
  attr_accessor :price
end

menu1 = Menu.new
```

### - Using Instances Variables

```ruby
class Menu
  attr_accessor :name
  attr_accessor :price
end

menu1 = Menu.new
menu1.name = "Sushi"
menu1.price = 20

puts "Harga dari Sushi per porsi adalah Rp#{menu1.price}"
```

```console
Harga dari Sushi per porsi adalah Rp20
```

### - Multiple Instances

```ruby
class Menu
  attr_accessor :name
  attr_accessor :price
end

menu1 = Menu.new
menu1.name = "Sushi"
menu1.price = 20

menu2 = Menu.new
menu2.name = "Pizza"
menu2.price = 10

puts "Harga dari #{menu1.name} per porsi adalah Rp#{menu1.price}"
puts "Harga dari #{menu2.name} per porsi adalah Rp#{menu2.price}"
```

```console
Harga dari Sushi per porsi adalah Rp20
Harga dari Pizza per porsi adalah Rp10
```

## **J. Instance Methods**

### - Using Methods

```ruby
class Menu
  attr_accessor :name
  attr_accessor :price
  
  # Define the info method
  def info
    puts "The name and the price will be printed"
  end
end

menu1 = Menu.new
menu1.name = "Pizza"
menu1.price = 8

# Call the info instance method of the menu1 instance
menu1.info
```

```console
The name and the price will be printed
```

### - Instance Methods

```ruby
class Menu
  attr_accessor :name
  attr_accessor :price
  
  def info
    # Return "The name and the price will be printed"
    return "The name and the price will be printed"
  end
end

menu1 = Menu.new
menu1.name = "Pizza"
menu1.price = 8

# Print the return value of the info instance method of the menu1 instance
puts menu1.info
```

```console
The name and the price will be printed
```

### - Methods and Instances Variables

```ruby
class Menu
  attr_accessor :name
  attr_accessor :price
  
  def info
    # Fill in the #{}
    return "#{self.name} $#{self.price}"
  end
end

menu1 = Menu.new
menu1.name = "Pizza"
menu1.price = 8

puts menu1.info
```

```console
Pizza $8
```

### - Classes and Instances Review

```ruby
class Menu
  attr_accessor :name
  attr_accessor :price
  
  def info
    return "#{self.name} $#{self.price}"
  end
  
  # Define the get_total_price method
  def get_total_price(count)
    total_price = self.price * count
    if count >= 3
      total_price -= 1
    end
    return total_price
  end
  
end

menu1 = Menu.new
menu1.name = "Pizza"
menu1.price = 8

# Print the return value of the get_total_price method of the menu1 instance

puts menu1.get_total_price(3)
```

```console
23
```

### - The Initialize Method

```ruby
class Menu
  attr_accessor :name
  attr_accessor :price
  
  # Define the initialize method
  def initialize
    self.name = "Pizza"
    self.price = 8
  end
  
  def info
    return "#{self.name} $#{self.price}"
  end
  
  def get_total_price(count)
    total_price = self.price * count
    if count >= 3
      total_price -= 1
    end
    return total_price
  end
end

menu1 = Menu.new
menu2 = Menu.new

# Print the return value of the info instance method of the menu1 instance
puts menu2.info
```

```console
Pizza $8
```

### - The Initialize Method 2

```ruby
class Menu
  attr_accessor :name
  attr_accessor :price
  
  # Rewrite the initialize method
  def initialize(name:,price:)
    self.name = name
    self.price = price
  end
  
  def info
    return "#{self.name} $#{self.price}"
  end
  
  def get_total_price(count)
    total_price = self.price * count
    if count >= 3
      total_price -= 1
    end
    return total_price
  end
end

# Add keyword arguments for name and price
menu1 = Menu.new(name: "Sushi", price: 10)
menu2 = Menu.new(name: "Pizza", price: 15)

puts menu2.info
```

```console
Pizza $15
```
# **Food Ordering App**
## - Separating Files
```ruby
# index.rb
require "./menu"

menu1 = Menu.new(name: "Sushi", price: 10)

puts menu1.info
```

```ruby
# menu.rb
class Menu
  attr_accessor :name
  attr_accessor :price
  
  def initialize(name:, price:)
    self.name = name
    self.price = price
  end
  
  def info
    return "#{self.name} $#{self.price}"
  end
  
  def get_total_price(count)
    total_price = self.price * count
    if count >= 3
      total_price -= 1
    end
    return total_price
  end
end
```

```console
Sushi $10
```

## - Displaying Menu
```ruby
# menu.rb
class Menu
  attr_accessor :name
  attr_accessor :price
  
  def initialize(name:, price:)
    self.name = name
    self.price = price
  end
  
  def info
    return "#{self.name} $#{self.price}"
  end
  
  def get_total_price(count)
    total_price = self.price * count
    if count >= 3
      total_price -= 1
    end
    return total_price
  end
end
```


```ruby
# index.rb
require "./menu"

menu1 = Menu.new(name: "Pizza", price: 8)
menu2 = Menu.new(name: "Sushi", price: 10)
menu3 = Menu.new(name: "Cola", price: 3)
menu4 = Menu.new(name: "Tea", price: 2)

menus = [menu1, menu2, menu3, menu4]

# Set the index variable to 0
index = 0

menus.each do |menu|
  # Print the index and the info of the menu instance
  puts "#{index}. #{menu.info}"
  # Update the index variable by adding 1 to it
  index += 1
end

```

```console
0. Pizza $8
1. Sushi $10
2. Cola $3
3. Tea $2
```

## - Receiving Input
```ruby
puts "Please enter your name"

# Receive input, then assign it to the name variable
name = gets.chomp

# Print "Hello, ____"
puts "Hello, #{name}"

puts "This cake costs $2"
puts "How many would you like to buy?"

# Receive input, then assign it to the count variable as an integer
count = gets.chomp.to_i

# Assign 2 * count to the total_price variable
total_price = 2 * count

# Print "The total price is $____"
puts "The total price is $#{total_price}"

```

```console
Please enter your name
Lerian
Hello, Lerian
This cake costs $2
How many would you like to buy?
```

## - Selecting a Menu
```ruby
# menu.rb
class Menu
  attr_accessor :name
  attr_accessor :price
  
  def initialize(name:, price:)
    self.name = name
    self.price = price
  end
  
  def info
    return "#{self.name} $#{self.price}"
  end
  
  def get_total_price(count)
    total_price = self.price * count
    if count >= 3
      total_price -= 1
    end
    return total_price
  end
end
```

```ruby
# index.rb
require "./menu"

menu1 = Menu.new(name: "Pizza", price: 8)
menu2 = Menu.new(name: "Sushi", price: 10)
menu3 = Menu.new(name: "Cola", price: 3)
menu4 = Menu.new(name: "Tea", price: 2)

menus = [menu1, menu2, menu3, menu4]

index = 0
menus.each do |menu|
  puts "#{index}. #{menu.info}"
  index += 1
end

puts "--------------"
puts "Select an item by its number:"

# Receive input, then assign it to the order variable as an integer
order = gets.chomp.to_i

# Assign the selected menu to the selected_menu variable
selected_menu = menus[order]

# Print "You have selected: ____"
puts "You have selected: #{selected_menu.name}"

puts "How many?(Buy 3 or more for $1 discount):"

# Receive input, then assign it to the count variable as an integer
count = gets.chomp.to_i

# Print "The total price is $____"
puts "The total price is $#{selected_menu.get_total_price(count)}"
```


```console
0. Pizza $8
1. Sushi $10
2. Cola $3
3. Tea $2
--------------
Select an item by its number:
0
You have selected: Pizza
How many?(Buy 3 or more for $1 discount):
2
The total price is $16
```

# **Class Inheritance**
## 1. Class Inheritance
```ruby
# menu.rb
class Menu
  attr_accessor :name
  attr_accessor :price
  
  def initialize(name:, price:)
    self.name = name
    self.price = price
  end
  
  def info
    return "#{self.name} $#{self.price}"
  end
  
  def get_total_price(count)
    total_price = self.price * count
    if count >= 3
      total_price -= 1
    end
    return total_price
  end
end
```

```ruby
# food.rb
require "./menu"

class Food < Menu

end
```

```ruby
# food.rb
require "./menu"

class Drink < Menu

end
```

## 2. How Inheritance Works

```ruby
# food.rb
require "./menu"

class Food < Menu

end
```

```ruby
# food.rb
require "./menu"

class Drink < Menu

end
```

```ruby
# index.rb
require "./food"
require "./drink"

food1 = Food.new(name:"Pizza",price:8)
puts food1.info
drink1 = Drink.new(name:"Cola",price:3)
puts drink1.info
```

```console
Pizza $8
Cola $3
```

## 3. Adding Instance Variables


```ruby
# food.rb
require "./menu"

class Food < Menu
  attr_accessor :calorie
end
```

```ruby
# food.rb
require "./menu"

class Drink < Menu
  attr_accessor :volume
end
```

```ruby
# index.rb
require "./food"
require "./drink"

food1 = Food.new(name:"Pizza",price:8)
food1.calorie = 700
puts food1.calorie
drink1 = Drink.new(name:"Cola",price:3)
drink1.volume = 500
puts drink1.volume
```

```console
700
500
```