# 100 Days Of Code - Log
#100DaysOfCode 2nd_rap Day: 001/100  
I am going to try for 2nd rap from today!  
I learned Linux command "nslookup".  
It is used to check the status of DNS server settings. And to check DNS-related setting in DNS clients.  
To use "nslookup command" , I need to install a package called "dnsutils"  

```bash
$ sudo apttitude install dnsutils
```
```bash
$ nslookup tatatamaki.com
Server:		133.***.*.***
Address:	133.***.0.3#53

Non-authoritative answer:
Name:	tatatamaki.com
Address: 133.***.**.***
```
#100DaysOfCode 2nd_rap Day: 002/100
I have created an MyMyCertificate.
I make three files.
- Private key server.key
- CSR server.csr
- CRT server.crt

$ openssl genrsa 2048 > server.key
$ openssl req -new -key server.key > server.csr
$ openssl x509 -days 3650 -req -signkey server.key < server.csr > server.crt

Then, I write the necessary information in the configuration file.
Normally, this would work, but it didn't.
Why?? MyMyCertificate !!

Life and programming don't always work out according to the manual...Aww
I will try again tomorrow !!

#100DaysOfCode 2nd_rap Day: 003/100
I try At Coder from today.
I learned the "gets method", the "split method".
The "gets method" is a method to get the value entered by the keyboard from the terminal as a string.
The "split method" splits the string with the specified delimiter and returns it as an array.
Code to determine whether a number is even or odd.
It is passed as a, b in the standard input(STDIN).

a, b = gets.split(' ')
ax = a.to_i
by = b.to_i
c = ax * by

if c.even?
	puts "Even"
else
	puts "Odd"
end

#100DaysOfCode 2nd_rap Day: 004/100
I try AtCoder.
https://atcoder.jp/contests/abs/tasks/abc081_a
It was supposed to be the easiest problem, but it was too hard.
But I cleard it.
The key is to write a one-line map(block)sentence.

arry = gets.chars
total = arry.map { |n| n.to_i }

p total.count(1)

#100DaysOfCode 2nd_rap Day: 005/100
I read about recursive functions today.
https://qiita.com/drken/items/23a4f604fa3f505dd5ad#fn1
This is a broad concept. As long as it calls itself, it is recursive.

def sum(arry)
	return 0 if arr.empty?
	top = arry.shift
	top + sum(arry)
end
p sum([1,2,3,4,5]) #=> 15

#100DaysOfCode 2nd_rap Day: 006/100

I learned Proc Object.
I want to use block as objects.
So, Proc is an object of the Block.
Add a parameter with & to the end of the temporary argument of a method definition.
hoge → Proc Object, &hoge → block

def foo_method(&hoge)
p hoge.call
end

foo_method { "test" }
=> "test"

#100DaysOfCode 2nd_rap Day: 007/100
I review for_syntax.
The process is repeated.
And, extract the elements from the array one by one and display them respectively. 

names = ['jhon', 'paul', 'george', 'ringo']
for name in names
puts name
end

#100DaysOfCode 2nd_rap Day: 008/100
I tried AtCoder. (ABC081B - Shift only)
I use "while sentence".
When the condition (if % 2 == 0) is met, assign the number divided by 2 to the variable i, and perform loop processing.
And, when the boolean is true, count is increased by 1.
When the boolean is false, it is out of the block.
Count will be assigned to the result variable as the return value.
Finally, in "result.min", output the smallest number among the return values.

n = gets.chomp.to_i
arry = gets.chomp.split(" ").map(&:to_i)

result = arry.map do |i|
	count = 0
	while i % 2 == 0 do
		i = i /2
		count += 1
	end
	count
end
puts result.min

#100DaysOfCode 2nd_rap Day: 009/100
Let's review "Hash" today !
What is "Hash" ?
An object of the Hash class that manages multiple data with a set of key/value combinations.
Can change the value by specifying a key.
Usse symbols, not strings, for hash keys!
But, I love Keith Richards better than Hash key !!

TheRollingStones = { Mick: "vacal", keith: "guitar", Ron: "guitar", Charlie: "Drums" }
	TheRollingStones.each do | name, part |
	puts "#{name} plays #{part}"
end

#100DaysOfCode 2nd_rap Day: 010/100
Self-assignment operator using || in Ruby.
a ||= 10 will return 10 if the variable a does not exist (nil or false).
a = nil or false
a ||= 10
=> 10

But、if the variable contains a value, assign it to a and use it as the return value.
a = 20
a ||= 10
=> 20

#100DaysOfCode 2nd_rap Day: 011/100
I create sql table.
The basics of the SELECT statement.

CREATE TABLE table_name
(
column_name data_type constraints,
shohin_mei CHAR(4) NOT NULL
);

The columns of the got table can be output.
SELECT get_column_name, get_column_name,,,,
FROM table_name;

And, if you specify a condition, it will retrieve the data that meets the condition.
SELECT shohin_mei, shohin_bunrui
FROM shohin
WHERE shohin b_bunrui = 'foo';

#100DaysOfCode 2nd_rap Day: 012/100
I tried AtCoder. (A - Century)
This question's point is Algorithm and .floor method.

n = gets.chomp.to_i
x = (n + 99) / 100
puts x.floor

When I was solving this problem, I thought again today. 
I'm not very good at thinking of algorithms.
It's fatal, but I have to do a lot of work and get used to the patterns.

I remember famous Japanese comedians saying, "Other people's children and bitter melons grow up fast."
Others are strangers. Don't worry about it!
Is it possible for adults to improve their academic skills in a subject they are not good at? It's an experiment with my own body!
I will do my best!!

#100DaysOfCode 2nd_rap Day: 013/100
I tried AtCoder. (A - Square Inequality )
No particular point.
It's a redundant code, but I did it without looking anything up just to make it work.

arry = gets.split(" ").map { |n| (n.to_i) **2 }

if arry[0] + arry[1] < arry[2]
puts "Yes"
else
puts "No"
end

#100DaysOfCode 2nd_rap Day: 014/100
I tried AtCoder. (A. Div)
Today's problem was not specifically related to ruby.
Just read the question text and answer.
Literacy is important.

n = gets.chomp.to_i
puts n-1

#100DaysOfCode 2nd_rap Day: 015/100
I tried AtCoder.(A. Rotate)

This sentence will cause an error.
arry = gets.split('')
s = arry.rotate
puts s.join('')

It was cause O.k.2
s = gets
puts s[1]+s[2]+s[0]

W~h~y~ AtCoder~?? said.(In the style of Atsugiri_Jason.)
I don't have a choice. I'll settle for this.

#100DaysOfCode 2nd_rap Day: 016/100
I tried AtCoder.(A - Difference Max)

I wrote first code. But, this code is error.
ab = gets.split(' ')
front_part = ab.max.to_i
cd = gets.split(' ')
back_part = cd.min.to_i
puts front_part - back_part

It is next code. But, this code is error. 
ab = gets.split(' ').max.to_i
cd = gets.split(' ').min.to_i
puts ab - cd

Third time's a charm !!
Success!!!
a, b = gets.split.map(&:to_i)
c, d = gets.split.map(&:to_i)
puts [a, b].max - [c, d].min

#100DaysOfCode 2nd_rap Day: 017/100
I tried AtCoder.(A - Health M Death)
This time, I was able to attack it simply with an "if statement".
The point is to perform a surplus calculation(operator => %).

m, h = gets.split.map(&:to_i)
if h % m == 0
puts "Yes"
else
puts "No"
end

#100DaysOfCode 2nd_rap Day: 018/100
I tried AtCoder.(A - I Scream)
This is an ice cream problem.
I'm going to have ice cream today.
A taste of home after a long absence, Blue Seal !!

a, b = gets.split.map(&:to_i)
	if a + b >= 15 && b >= 8
		puts 1 
	elsif a + b >= 10 && b >= 3
		puts 2
	elsif a + b >= 3
		puts 3
	else
		puts 4
	end

#100DaysOfCode 2nd_rap Day: 019/100
I tried AtCoder.(A - Discount)
Use method String#to_f to get the decimal point.
You get what you pay for.

a, b = gets.split.map(&:to_f)
discount = (1 - b / a) * 100
p discount

#100DaysOfCode 2nd_rap Day: 020/100
I tried AtCoder.(A - Star)
I remembered the Fizzbuzz Quiz.
Good old days~!

x = gets.chomp.to_i
(1..100).each do |n|
	if (x + n)  % 100 == 0
		puts n
	else
		next
	end
end

#100DaysOfCode 2nd_rap Day: 021/100
I tried AtCoder.(A - Vanishing Pitch)
Use the conditional operator　"||".
Lately, I've been enjoying watching Major League Baseball player Otani's activities !!
Big fly !! OooootaniSaaaan !!

v, t, s, d = gets.split.map(&:to_i)
invisible_ball_start = v * t
invisible_ball_finish = v * s
if invisible_ball_start > d || invisible_ball_finish < d
puts "Yes"
else
puts "No"
end

#100DaysOfCode 2nd_rap Day: 022/100
I tried AtCoder.(A - Very Very Primitive Game)
It took me a long time.
In the end, the output was just the opposite.
Fall and fall, but I get up and keep going. Like a Rolling stone !!

a, b, c = gets.split.map(&:to_i)
if c == 0 && a <= b
puts "Aoki"
elsif c == 1 && a < b
puts "Aoki"  
else
puts "Takahashi"
end

a, b, c = gets.split.map(&:to_i)
if c == 0
puts a <= b ? "Aoki" : "Takahashi"
elsif c == 1
puts a < b ? "Aoki" : "Takahashi"
end

a, b, c = gets.split.map(&:to_i)
if c == 0 && a <= b
puts "Aoki"
elsif c == 0 && a > b
puts "Takahashi"
elsif c == 1 && a < b
puts "Aoki"
elsif c == 1 && a >= b
puts "Takahashi"
else
puts  "Aoki"
end

#100DaysOfCode 2nd_rap Day: 023/100
I tried AtCoder.(A - Slot)
I would like to use a method and go for it, but I'm not sure what I'm capable of right now.
Keep trying!!

c = gets.to_s.chars
if c[0] == c[1] && c[1] == c[2]
puts "Won"
else
puts "Lost"
end

#100DaysOfCode 2nd_rap Day: 024/100
I tried AtCoder.(A - Three-Point Shot)
Received as an array, sorted, and calculated.
It's so redundant!
Redundant, which sounds like Linda Linda.
A punk band apparently named after a Japanese punk band(THE BLUE HEARTS).
COOL !!
https://twitter.com/LAPublicLibrary/status/1395485852579495936?s=20

arry = gets.to_s.split.map{ |e| e.to_i }
s = arry.sort
score = s[1] - s[0]
result = score < 3 ? "Yes" : "No"
puts result

#100DaysOfCode 2nd_rap Day: 025/100
I forgot to tweet this yesterday.
Guard Clause is one of the techniques to avoid deep nesting of conditional branches, 
and is sometimes translated as "guard clause", "guard condition", or "guard syntax".
It is sometimes referred to as "early return" because of its behavior.

def ranking(point)
return 'gold' if point > 90
return 'silver' if point > 70
return 'bronze' if point > 50
'PrizeForParticipation'
end

#100DaysOfCode 2nd_rap Day: 026/100
I tried AtCoder.(A - Brick)
I'm getting used to that A problem.
Let's work on problem B next time.

n, w = gets.split.map(&:to_i)
brick = n / w
puts brick

#100DaysOfCode 2nd_rap Day: 027/100
I tried AtCoder.(B - 180°)
First try B problem.
It was difficult, but I managed to get through it.
Keep going !!

s = http://gets.to_s.split("")
x = s.reverse.join
y = http://x.tr('69', '96')
puts y

#100DaysOfCode 2nd_rap Day: 028/100
I tried AtCoder.(A - ABC Preparation)
Today first, I tried problem B, but it was too difficult to solve.
I had to start from problem A again.

a = gets.to_s.split.map{ |e| e.to_i }
puts a.min 

#100DaysOfCode 2nd_rap Day: 029/100
Today, I studied about "Shinara".
"Sinatra" is Web Application Framework.
"Sinatra" is very hard. But, I keep is going!!
Because, "That's life ♪"
And,
I'm trying with the A problem challenge.
(A - Determinant)

a, b = gets.to_s.split.map{ |e| e.to_i }
c, d = gets.to_s.split.map{ |e| e.to_i }
puts result = a * d - b * c

#100DaysOfCode 2nd_rap Day: 030/100
Today, I studied JSON.
It is adopted a lightweight data representation format.
It is characterized by its ability to describe data structures that are easy to handle from programming languages, such as hashes and arrays.
Here are a few of the objects.
A set of names and values. A name/value pair is called a "memba" of an object.
It has four "membas" : name, nickname, age, and position.

{
"name" : {
"first": "shohei",
"last": "otani"
},
"nickname": "ooootanisaaan",
"age": 26,
"position": ["picher", "batter", "runner"]
}

#100DaysOfCode 2nd_rap Day: 031/100
I tried AtCoder.(B - Do you know the second highest mountain?)
B problem is difficult. I googled it.
I've turned to the sort_by method.
https://docs.ruby-lang.org/ja/latest/method/Enumerable/i/sort_by.html

n = gets.to_i
name_height = Array.new(n){gets.split}
puts name_height.sort_by{_2.to_i}[-2][0]

#100DaysOfCode 2nd_rap Day: 032/100
I tried AtCoder.(B - 200th ABC-200)
The point of today's problem is to use times_method.
And it's about using logic (n % 200 == 0).

n, k = gets.split.map(&:to_i)
k.times do |i|
if n % 200 == 0
n /= 200
else
n = n*1000 + 200
end
end
puts n

#100DaysOfCode 2nd_rap Day: 033/100
Minitest is a framework for testing.
Write "require 'minitest/autorun'".
Write the relative path to the file you want to test.
Specify with 'require_relative'.
Write the method name as "test_".
Check for methods marked with "test_".
"asset_equal" , if a and b are the same, pase. 

require 'minitest/autorun'
require_relative '../piyo/foobar'

class FooBar < Minitest::Test
def test_foobar
assert_equal b, a
end
end

#100DaysOfCode 2nd_rap Day: 034/100
I studied object-oriented.
I used is this book "https://www.shoeisha.co.jp/book/detail/9784798134659"
First of all, I learned 3 important Features of object-oriented.
- Inheritance Sharing the characteristics of a class. Abstraction <= Embodiment
- Encapsulation Clarify the scope of functions and data.
- Polymorphism Even if the class is the same, there are differences in the behavior of each object.
	Use properly.

#100DaysOfCode 2nd_rap Day: 035/100
I studied json_file's exporting & importing.

# How to convert a Hash to a JSON string and write it to a JSON file.
require 'json'
File.open("where to save the file", 'w') do |file|
str = JSON.dump(Export as a hash, file_object)
end

# Read a JSON file and convert it to Ruby Hash.
File.open("./sample.json") do |file|
hash = JSON.load(file)
p hash
end

#100DaysOfCode 2nd_rap Day: 036/100
A web system has a three-tier structure: web server, application server, and database server.
Thin, WEBrick is a member of the application server.

I try to use WEBrick.
# write to a Gemfile.
gem 'webrick'

# write to a myapp.rb file.
require 'webrick'

# I run what I wrote in my Gemfile.
bundle exec ruby myapp.rb

#100DaysOfCode 2nd_rap Day: 037/100
I tried AtCoder.(B - Intersection)
I used Ternary operator.
This "n = gets.to_i" doesn't make any particular sense,
but I've implemented it.
Using ternary operators is simple and cool!！

n = gets.to_i
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)
x = (b.min) - (a.max)
puts x >= 0 ? x+1 : 0

#100DaysOfCode 2nd_rap Day: 038/100
I tried AtCoder(B - Palindrome with leading zeros).
Very hard question...
But, I cleared it!
This question's point is regex "/0*&/".
By combining this regex with the sub method, I was able to create the process I wanted to get.
I'm tired today. I'll try again tomorrow!!
[String\#sub \(Ruby 3\.0\.0 リファレンスマニュアル\)](https://docs.ruby-lang.org/ja/3.0.0/method/String/i/sub.html)
n = gets.chomp.to_s
x = n.sub(/0*$/, "")
if n == n.reverse
puts "Yes"
elsif x == x.reverse
puts "Yes"
else
puts "No"
end

#100DaysOfCode 2nd_rap Day: 039/100
I studied Test Driven Development.
The steps of the TDD cycle.
1. Think about your next goal.
2. write a test that demonstrates that goal
3. run that test and make it fail (Red)
4. write the code for the goal
5. make the test you wrote in step 2 succeed (Green)
6. refactor the code until the test passes (Refactor)
7. repeat steps 1~6
Point is writing from the goal.
Think small and build up.

#100DaysOfCode 2nd_rap Day: 040/100
I studies inject method.
It's called the method of doing Convolution operation.
I really don't know what that means mathematically.It's really hard.
For now, I understand it as Ruby's method.

Step1, The first iteration will put # in hex.
Step2, The string created by "hex + n.to_s(16).rjust(2, '0')" in the block will go into hex in the next iteration.
Step3, When the iteration process reaches the end, the return value of the block becomes the return value of the inject method itself.

n.to_s(16).rjust(2, '0')
def to_hex(r, g, b)
[r, g, b].inject('#') do |hex, n|
hex + n.to_s(16).rjust(2, '0')
end
end

#100DaysOfCode 2nd_rap Day: 041/100
I tried AtCoder(A \- Rock\-paper\-scissors).
I also tried to test code today.
I used the knowledge,  I learned in the circle reading session.
Nice autput !! keep going!

x, y = gets.split.map(&:to_i)
def atcoder(x, y)
if x == y
x
else
3 - x - y
end
end

require 'minitest/autorun'

class AtcoderTest < Minitest::Test
def test_atocoder
assert_equal 1, atcoder(2,0)
assert_equal 2, atcoder(2,2)
end
end

#100DaysOfCode 2nd_rap Day: 042/100
Caution! About the type of the hash key.
I've been wrong about hash key all this time.
If the key type is string, specify string.
If it is a symbol, specify the symbol.

<h1>memo</h1>
<div class="index">
<p><%= @hash["title"] %></p>
<p><%= @hash["content"] %></p>
</div>

#100DaysOfCode 2nd_rap Day: 043/100
I tried AtCoder(A - kcal)
I wrote some more test code today.
And, I wrote according to the procedure in the TDD rules.

a, b = gets.split.map(&:to_f)
def kcal(a, b)
puts b / 100 * a
end

require 'minitest/autorun'
class KcalTest < Minitest::Test
def test_kcal
assert_equal 90, kcal(45, 200)
end
end

#100DaysOfCode 2nd_rap Day: 044/100
I tried AtCoder(A - ABC Preparation)
For the first time, I could write one line of code !!

puts  gets.to_s.split.map(&:to_i).min

And, I wrote test code ver.

def abc(arry)
 arry.to_i
end

arry = gets.to_s.split.map(&:to_i).min
abc(arry)

require 'minitest/autorun'

class AbcTest < Minitest::Test
def test_abc
assert_equal 3, abc(3)
end
end

#100DaysOfCode 2nd_rap Day: 045/100
I studied about splat deployment.
This is used when you want to expand an array and pass it as multiple arguments.
It can also be used as a method argument.

irb(main):009:1* def greeting(*names)
irb(main):010:1*   "#{names.join(' and ')} say, Hello"
irb(main):011:0> end
=> :greeting
irb(main):012:0> greeting('Jhon','Paul')
=> "Jhon and Paul say, Hello"

#100DaysOfCode 2nd_rap Day: 046/100
I tried AtCoder(B - Nuts)
It was difficult to pass arguments to the method.
It passed the test successfully.
This time, I passed an array as the argument, but if it is a string, use *arry to expand the splat.

a = [6,17,28]

def nuts(arry)
total = 0
arry.each do |x|
if x > 10
total += (x - 10)
end
end
total
end

require 'minitest/autorun'

class NutsTest < Minitest::Test
def test_nuts
assert_equal 25, nuts([6,17,28])
end
end

#100DaysOfCode 2nd_rap Day: 047/100
Today I reviewed　about Guard Clause.
Basic Form　=> return foo if bar
It is said that it is good manners to leave the bottom line of a sentence with a guard clause blank.

As an aside...
Today is PaulMcCartney Birthday !!
irb(main):016:1* def play(name)
irb(main):017:1*   return 'name,Please' if name.nil?
irb(main):018:1*
irb(main):019:2*   if name == 'Paul'
irb(main):020:2*     'I play bass guitar!'
irb(main):021:2*   elsif name == 'Ring'
irb(main):022:2*     'I play drums!'
irb(main):023:2*   else
irb(main):024:2*     'I play guitar'
irb(main):025:1*   end
irb(main):026:0> end
=> :play
irb(main):027:0> play('Paul')
=> "I play bass guitar!"
irb(main):028:0> play(nil)
=> "name,Please"
irb(main):029:0>


#100DaysOfCode 2nd_rap Day: 048/100
I tried AtCoder(B - AtCoder Condominium)
I used Convolution operation today.
Code is easy but, It was hard to come up with logic.

a, b = gets.to_s.split.map(&:to_i)

n = (1..a).map{|i| i * 100}
sum_n = n.inject(0) {|result, n| result + n} * b
k = (1..b).map{|i| i += 0}
sum_k = k.inject(0) {|result, k| result + k} * a
puts sum_n + sum_k

#100DaysOfCode 2nd_rap Day: 049/100
"Ruby feels good when I get it right!!"
Here's what Matz had to say. 
I've been thinking about my experiences with Ruby and how good it felt.
My first experience is with the ternary operator.

Before refactoring.
`shots = []
scores.each do |s|
shots << if s == 'X'
10
else
s.to_i
end
end`

After code.
Good feeling !!!!!
`scores.each { |s| shots << ( s == 'X' ? 10 : s.to_i ) }`

Then, I got a review and was able to make it even shorter.
shots = scores.map{|s| s == 'X' ? 10 : s.to_i }`

#100DaysOfCode 2nd_rap Day: 050/100
I wrote the Sinatra program about memo app.
Today, I created edit page.
It's difficult. 
I hope to have it done by the end of the week.

<h1>memo</h1>
<form action="/memos/:id" method="patch">
  <% @memo.each do |memo| %>
    <% "#{memo["id"]}" %>
    <p class="title">title</p>
    <textarea name="title" id="title"><%= "#{memo["title"]}" %></textarea></P>
    <p>内容</p>
    <p><textarea name="content" id="content"><%= "#{memo["content"]}" %></textarea></p>
    <p><input type="submit" value="Save"></p>
    <p><a href='/memos'>Top</a></p>
    <p><a href='/memos/new'>New</a></p>
    <p><a href='/memos/<%= memo["id"] %>'>Back</a></p>
  <% end %>
</form>

#100DaysOfCode 2nd_rap Day: 051/100
I was thinking about the theme of the LT meeting.
I checked the past daily reports and other documents.
I found a FizzBuzz problem and tried to solve it with ternary operators.
I do this today for a change.
Maybe,
You can make it shorter.

def fizz_buzz(x)
(x..100).each do |n|
puts (n % 15).zero? ? 'Fizz_Buzz': n.to_s
puts (n % 3).zero? ? 'Fizz' : n.to_s
puts (n % 5).zero? ? 'Buzz' : n.to_s
puts n.to_s
end
end

fizz_buzz(1)

#100DaysOfCode 2nd_rap Day: 052/100
I learned about HTTP routing.
I've been thinking about it all day.
And, I've been working on the code all day.
It's been a fucking exhausting day...
But, I've leveled up.

Don't stop learning !!

<h1>memo</h1>
<% @memo.each do |memo| %>
<form action="/memos/<%= memo["id"] %>" method="post">
    <input type="hidden" name="_method" value="patch">
    <p class="title">title</p>
    <p><textarea name="title" id="title"><%= "#{memo["title"]}" %></textarea></P>
    <p>内容</p>
    <p><textarea name="content" id="content"><%= "#{memo["content"]}" %></textarea></p>
    <p><input type="submit" value="保存"></p>
    <p><a href='/memos'>top</a></p>
    <p><a href='/memos/new'>new</a></p>
    <p><a href='/memos/<%= memo["id"] %>'>戻る</a></p>
  <% end %>
</form>

#100DaysOfCode 2nd_rap Day: 053/100
I tried AtCoder(A - Determinant)
a, b = gets.to_s.split.map{ |e| e.to_i }
c, d = gets.to_s.split.map{ |e| e.to_i }
def atcoder(a, b, c, d)
a * d - b * c
end

require 'minitest/autorun'

class AtcoderTest < Minitest::Test
def test_atocoder
assert_equal -2, atcoder(1,2,3,4)
assert_equal -2, atcoder(2,3,4,5)
end
end

#100DaysOfCode 2nd_rap Day: 054/100
I tried AtCoder(A - ReLU)
For now, today, 
I decided to use the ternary operator.
It was the fastest way to solve the problem.

x = gets.to_s.to_i
puts x >= 0 ? x : 0

#100DaysOfCode 2nd_rap Day: 055/100
I tried AtCoder(A - twiblr)
Today, I thought about the theme of the LT.
I finally decided on a theme: I'll talk about JSON files and Hash tags.and, about  creating a memo's application using sinatra.

a, b = gets.split.map(&:to_i)
puts  (2*a + 100) - b

#100DaysOfCode 2nd_rap Day: 056/100
I did some code refactoring.

post '/memos/:id' do
memo = {
"id" => SecureRandom.uuid,
"title" => params["title"],
"content" => params["content"],
"created_at" => Time.now
}
File.open("./db/memos_#{memo["id"]}.json", 'w') do |file|
JSON.dump(memo, file)
end
redirect to('/memos')
end

#100DaysOfCode 2nd_rap Day: 057/100
Today, The skeleton of the memo app is complete.
I implemented File.delte mehotd.
Next, arrange the design in css.

delete '/memos/:id' do
memo = { "id" => params["id"], "title" => params["title"], "content" => params["content"], "created_at" => "Time.now"}
File.delete("./json/memos_#{memo["id"]}.json")
redirect to("/memos")
end

<h1>メモしやがれ</h1>
<% @memo.each do |memo| %>
  <form action="/memos/<%= memo["id"] %>" method="post">
    <input type="hidden" name="_method" value="delete">
    <p class="title">タイトル</p>
    <p><textarea name="title" id="title" readonly="readonly"><%= "#{memo["title"]}" %></textarea></P>
    <p>内容</p>
    <p><textarea name="content" id="content" readonly="readonly"><%= "#{memo["content"]}" %></textarea></p>
    <p><input type="submit" value="削除"></p>
    <p><a href='/memos'>トップページ</a></p>
    <p><a href='/memos/<%= memo["id"] %>'>戻る</a></p>
    <p><a href='/memos/<%= memo["id"] %>/edit'>編集ページ</a></p>
<% end %>
  </form>

#100DaysOfCode 2nd_rap Day: 058/100
I participated in the LT meeting today and gave a presentation.
It was great to be able to rehearse with the school mentor and get feedback.
After listening to the content of the other speakers, I realized that I still need to work harder.
I'd like to keep learning !!

I understood Enumerator_class today.
Enumerator_class includes the Enumerable_module.

#100DaysOfCode 2nd_rap Day: 059/100
Today I was writing css for my own memo application.
It's been a while since I wrote it, so I forgot about it.
I wrote it while researching.
I'm about 80% done.
I hope to finish it tomorrow.

body {
font-family: 'Reggae One', cursive;
}
.container {
background-color: rgb(245,241,130);
width: 400px;
}
...more

#100DaysOfCode 2nd_rap Day: 060/100
Today, I continued with the creation of the memo application.
The CSS style implementation is complete.
Title mean is "Make a note!!"
I paid homage to the first album of the Sex Pistols.
It was inspired by the design of Sex Pistols first album.

#100DaysOfCode 2nd_rap Day: 061/100
What to do when you want a JSON string to be returned as a symbol when returning it as a hash object.
Add an option when converting JSON format strings to hash objects.
[JSON\.\#parse \(Ruby 3\.0\.0 リファレンスマニュアル\)](https://docs.ruby-lang.org/ja/3.0.0/method/JSON/m/parse.html)

get '/memos' do
files = Dir.glob('./json/*.json')
@memos = files.map { |f| JSON.parse(File.open(f).read, symbolize_names: true) }
@memos = @memos.sort_by { |f| f['created_at'] }
erb :index
end

#100DaysOfCode 2nd_rap Day: 062/100
I wrote README.md, today.
Git is difficult. I can't make pull-links well.
I'll try again tomorrow.

Name
メモしやがれ

Description
Sinatraを使って作成したメモアプリです。 メモの新規作成、編集、削除が行えます。

Demo
Image from Gyazo

install
任意のディレクトリへ移動し、以下でGitHubリポジトリをクローンしてください。

\$ git clone https://github.com/shirotamaki/sinatra_memo_app.git
inatra_memo_app ディレクトリへ移動してください。

\$ cd sinatra_memo_app
bundle install を実行し、必要なGemをインストールしてください。

& bundle install
myapp.rbをrubyコマンドで実行すると、Sinatraを使ってサーバーが起動します。

\$ ruby myapp.rb
ブラザウザへ下記URIを入力してください。 http://localhost::4567/memos

#100DaysOfCode 2nd_rap Day: 063/100
I made a new discovery about rubocop.
Rubocop is designed to check ruby code, and does not support erb files.
Since RuboCop itself is a big gem, there are people who think the same thing like "can't we do it in erb?" or "I wish we could do it in erb", And there is such an Issue standing.
In response to this, Mr.bbatsov, who is probably the administrator, replied,
He says "It's outside the scope of RuboCop."
https://github.com/rubocop/rubocop/issues/1113

#100DaysOfCode 2nd_rap Day: 064/100
I learned debug methods.
I tried Byebug.
After invoking Byebug, 
I can use help + command_name to display the description and shortened command.

[2, 11] in /Users/shiro/ruby-practices/01.fizzbuzz/test/fizz_buzz_test.rb
2: require_relative '../lib/fizzbuzz'
3:
4: class FizzBuzzTest < Minitest::Test
5:   def test_fizz_buzz
6:     require 'byebug'; byebug
=>  7:     assert_equal '1', fizz_buzz(1)
8:     assert_equal '2', fizz_buzz(2)
9:     assert_equal 'Fizz', fizz_buzz(3)
10:     assert_equal '4', fizz_buzz(4)
11:     assert_equal 'Buzz', fizz_buzz(5)
(byebug) help step

s[tep][ times]

Steps into blocks or methods one or more times

#100DaysOfCode 2nd_rap Day: 065/100
I reviewed the binding.irb that I was taught before.
I wrote 'bindin.irb'. That way, I can create a breakpoint.
So, irb will start, and I can type in the code, I want to try.

shiro@shiro:~/ruby-practices/01.fizzbuzz (wc_command *)$ ruby test/fizz_buzz_test.rb

From: /Users/shiro/ruby-practices/01.fizzbuzz/lib/fizzbuzz.rb @ line 12 :

     7:     "Buzz"
     8:   else
     9:     n.to_s
    10:   end
    11: end
=> 12: binding.irb
13:
14:
15: # require 'minitest/autorun'
16: #
17: # class FizzBuzzTest < Minitest::Test

irb(main):001:0> fizz_buzz(15)
=> "Fizz Buzz"
irb(main):002:0> fizz_buzz(99)
=> "Fizz"
irb(main):003:0> fizz_buzz(7)
=> "7"

#100DaysOfCode 2nd_rap Day: 066/100
It's been a while since I solved Atcoder today.
A problem. It's been a while, so I wasn't confident, but I was able to solve it.

A. twiblr
a, b = gets.split.map(&:to_i)
puts  (2*a + 100) - b

A. Heavy Rotation
a, b = gets.split.map(&:to_i)
puts  (2*a + 100) - b

A - box
n, a, b = gets.split.map(&:to_i)
puts n - a + b

#100DaysOfCode 2nd_rap Day: 067/100
I reviewed SQL today.
I set up the environment on my Mac OS.
Then I logged in and changed the user.
After that, I created a database, created tables, and added columns.
INSERT sentence and SELECT sentence.

shop=# select * from shohin;
shop=# INSERT INTO Shohin (shohin_id, shohin_mei, shohin_bunrui, hanbai_tanka, shiire_tanka, torokubi) VALUES ('0004', '時計', 'アクセサリ', 100000, 80000, '2021-07-07');
INSERT 0 1

#100DaysOfCode 2nd_rap Day: 068/100
I tried AtCoder(B - Palindrome with leading zeros)
It was difficult.

n = gets.chomp.to_s
x = n.sub(/0*$/, "")
if n == n.reverse
puts "Yes"
elsif x == x.reverse
puts "Yes"
else
puts "No"
end

#100DaysOfCode 2nd_rap Day: 069/100
I tried AtCoder(B - Many Oranges)
Today's problem was also difficult.....
Or rather, I almost couldn't solve it on my own.
I understand the ruby code, but I can't understand the problem itself.
Full search...

a,b,w = gets.split.map(&:to_f)
w = w*1000
if (w/a).floor < (w/b).ceil
puts  "UNSATISFIABLE"
else
puts "#{(w/b).ceil} #{(w/a).floor}"
end

#100DaysOfCode 2nd_rap Day: 070/100
I learned git.
Today I got the following command

git switch
git restore
git diff
git reflog
git cherry-pick
git stash
git grep

#100DaysOfCode 2nd_rap Day: 071/100
Today I refactored the memo application.
I understood RESTfull URI.

post '/memos' do
memo= { id: SecureRandom.uuid, title: params[:title], content: params[:content], created_at: Time.new }
File.open("./json/memos_#{memo[:id]}.json", 'w') do |file|
JSON.dump(memo,file)
end
redirect to("/memos/#{h(memo[:id])}")
end

#100DaysOfCode 2nd_rap Day: 072/100
I tried AtCoder(A - Plural Form)

n = gets.to_s.chomp
unless n[-1] == "s"
print n.concat "s"
else
print n.concat "es"
end

#100DaysOfCode 2nd_rap Day: 073/100
I thought about how to extract a json file.
It turns out that the return value is different for the pattern without the .first method and the pattern with it.
It unresolved.  But a step forward.未解決

irb(main):005:0> file = Dir.glob("./json/memos_f51cdea2-fb63-4167-91a1-ec642f875
06e.json")
=> ["./json/memos_f51cdea2-fb63-4167-91a1-ec642f87506e.json"]

irb(main):006:0> file = Dir.glob("./json/memos_f51cdea2-fb63-4167-91a1-ec642f875
06e.json").first
=> "./json/memos_f51cdea2-fb63-4167-91a1-ec642f87506e.json"

#100DaysOfCode 2nd_rap Day: 074/100
I tried AtCoder(A - Not)
x = gets.to_s.to_i
puts x == 0 ? 1 : 0

#100DaysOfCode 2nd_rap Day: 075/100
I studied PostgreSQL.
I made a database.
And, I created a table in that database and inserted data.
[ged/ruby\-pg: A PostgreSQL client library for Ruby](https://github.com/ged/ruby-pg)

#!/usr/bin/env ruby
require 'pg'

# Output a table of current connections to the DB
conn = PG.connect( dbname: 'postgres' )
conn.exec( "INSERT into piyo values ('05', 'title5', 'memo5' );" )
conn.exec( 'select * from piyo' ) do |result|
result.each do |row|
puts row
end
end

#100DaysOfCode 2nd_rap Day: 076/100
I tried AtCoder(A - Don't be late)
This is a problem where an integer is given, but sometimes the result is a decimal point when giving the speed in seconds.
For the reason, I used to_f method.

d, t, s = gets.split.map(&:to_f)
puts d/s <= t ? "Yes" : "No"

#100DaysOfCode 2nd_rap Day: 077/100
I tried AtCoder(A - Takoyaki)
Point is Float#ceil.
[Float\#ceil \(Ruby 3\.0\.0 リファレンスマニュアル\)](https://docs.ruby-lang.org/ja/3.0.0/method/Float/i/ceil.html)
def made_takoyaki(n, x, t)
puts ((n/x).ceil * t).to_i
end

n, x, t = gets.split.map(&:to_f)
made_takoyaki(n, x, t)

#100DaysOfCode 2nd_rap Day: 078/100
I tried AtCoder(A - Rainy Season)
It's a dirty fucking code....
But this is what I'm capable of now.
Studying again tomorrow !!

s = gets.to_s.chomp
if s == "RRR"
puts "3"
elsif s == "RRS"
puts "2"
elsif s == "SRR"
puts "2"
elsif s == "SSS"
puts '0'
else
puts "1"
end

#100DaysOfCode 2nd_rap Day: 079/100
I tried AtCoder(A - Air Conditioner)
First time!
I solved a problem in under two minutes!!!

x = gets.to_i
puts x >= 30 ? 'Yes' : 'No'

I'd also like to introduce this one, which I think is the fastest song in the world.
The pride of Japan, the Hardcore band BBQ CHICKENS!!!
https://open.spotify.com/track/7ITg3WkHWJoUyh9buVmHRM?si=e5aadb0e96b9476c

#100DaysOfCode 2nd_rap Day: 080/100
Today I learned about SQL Injection.
I had a hard time with 'placeholder', 
but I managed to complete the implementation!
Congratulations!!
Me!!
@memos = conn.exec('SELECT * FROM t_memos WHERE id = $1;', [params['id']])
conn.exec('INSERT INTO t_memos (title, content) VALUES ($1, $2);', [params['title'], params['content']])
conn.exec('UPDATE t_memos SET title = $1, content = $2 WHERE id = $3;', [params['title'], params['content'], params['id']])

#100DaysOfCode 2nd_rap Day: 081/100
I tried AtCoder(A - Payment)
n = gets.to_i
m = n / 1000
if n % 1000 != 0
m += 1
end
puts 1000 * m - n

#100DaysOfCode 2nd_rap Day: 082/100
n = gets.chomp.to_i
puts total = n + n**2 + n**3

https://docs.ruby-lang.org/ja/3.0.0/doc/symref.html

#100DaysOfCode 2nd_rap Day: 083/100
I tried AtCoder(A - alphabet)
I used a regular expression.
And, I used '=~' to compare conditions.

moji = gets.to_s.chomp
puts moji =~ /[A-Z?]/ ? 'A' : 'a'

#100DaysOfCode 2nd_rap Day: 084/100
I studied Activ_Record, migration_file.
It is code migration_file from Rails.
Line 3, Create a table named "books" with create_table :books.
Line 4, The value of t.string :title and the value of t.text :memo create the element of the table.

class CreateBooks < ActiveRecord::Migration[6.1]
def change
create_table :books do |t|
t.string :title
t.text :memo
      t.timestamps
    end
end
end

#100DaysOfCode 2nd_rap Day: 085/100
I tried AtCoder(A - Five Variables)
Today, I came up with two programs.

gets.split.map(&:to_i).each_with_index do |i, idx|
if i == 0
puts idx + 1
end
end

x = gets.split.map(&:to_i)
puts x.index(0)+1

#100DaysOfCode 2nd_rap Day: 086/100
I learned the nil guard, a commonly used idiom.
In this case, I wanted the variable to act like a cache.
This is where the nil guard comes into play.
I was able to implement it successfully.

class Memo
def conn
@connection ||= PG.connect(dbname: 'memos')
end
end

#100DaysOfCode 2nd_rap Day: 087/100
I tried AtCoder(A - Multiplication 1)
As expected, the problem was too easy, so I wrote it using classes.
There's a difference in difficulty even in A problems...

class Calculator
def calc(a, b)
puts @total = a * b
end
end

a, b = gets.split.map(&:to_i)
total = Calculator.new
total.calc(a, b)

#100DaysOfCode 2nd_rap Day: 088/100
I tried AtCoder(A - ∴ (Therefore))

n = gets.to_s.chomp
arry = n.chars.map(&:to_s)
m = arry[-1]

if m == '3'
puts 'bon'
elsif m ==  '0' || m == '1' || m == '6' || m == '8'
puts 'pon'
else
puts 'hon'
end

#100DaysOfCode 2nd_rap Day: 089/100
I tried AtCoder(A - Registration)
Today, I used chop methods.

s = gets.to_s.chomp
t = gets.to_s.chomp
puts s == t.chop ? 'Yes' : 'No'

#100DaysOfCode 2nd_rap Day: 090/100
I tried AtCoder(A \- A?C、A \- We Love Golf)

s = gets.to_s.chomp
puts s == 'ABC' ? 'ARC' : 'ABC'

k = gets.to_i
a, b = gets.split.map(&:to_i)

a.upto(b) do |n|
if n % k == 0
@flying_distance = 'OK'
break
end
end
puts @flying_distance ||= 'NG'

#100DaysOfCode 2nd_rap Day: 091/100
I tried AtCoder(A \- Sheep and Wolves, A \- Circle Pond)
I solved two problems.
s, w = gets.split.map(&:to_i)
puts s <= w ? 'unsafe' : 'safe'

r = gets.to_f
puts circle_pond = r * 2 * 3.14

#100DaysOfCode 2nd_rap Day: 092/100
Today, I tried to introduce the kaminari's gem for the assignment.
The basic implementation was done.

/app/controllers/books_controller.rb
def index
	@books = Book.page(params[:page]).per(2) 
end

/app/views/books/index.html.erb
<%= paginate @items %>

#100DaysOfCode 2nd_rap Day: 093/100
I tried AtCoder(A - Lucky 7)

n = gets.to_s.chomp
puts n.include?('7') ? 'Yes' : 'No'

#100DaysOfCode 2nd_rap Day: 094/100
I tried AtCoder(A -ABC Swap)

a, b, c = gets.to_s.split.map(&:to_s)
x, y, z = c, a, b
puts "#{x} #{y} #{z}"

arry = gets.split.map(&:to_i)
puts arry.rotate(2).join(' ')

The rotate method passes cnt as an argument, where cnt stands for count.
https://docs.ruby-lang.org/ja/3.0.0/method/Array/i/rotate.html

#100DaysOfCode 2nd_rap Day: 095/100
I tried AtCoder(A -Coffee)

S = gets.chomp.chars.map(&:to_s)
if S[2] == S[3] && S[4] == S[5]
puts 'Yes'
else
puts 'No'
end

#100DaysOfCode 2nd_rap Day: 096/100
I tried AtCoder(A -The Number of Even Pairs)
I understood this code.
But,Full exploration is difficult.

n, m = gets.split.map(&:to_i)
puts (n*(n-1)/2) + (m*(m-1)/2)

#100DaysOfCode 2nd_rap Day: 097/100
I tried AtCoder(A - Station and Bus)

S = gets.to_s.chomp.chars
puts S.uniq.count  >= 2 ? 'Yes' : 'No'

#100DaysOfCode 2nd_rap Day: 098/100
I tried AtCoder(A - Duplex Printing)

n = gets.to_i
puts (n+1) / 2

#100DaysOfCode 2nd_rap Day: 099/100
I tried AtCoder(A - Beginner)
n, r = gets.split.map(&:to_i)
if n < 10
puts r + (100*(10-n))
else
puts r
end

The point is to replace the equation with a formula and then think about it.
Don't think complicated. Keep it simple.
r = x- 100*(10-k)


#100DaysOfCode 2nd_rap Day: 0100/100
I tried AtCoder(A - Remaining Balls)
Today is 100days!! Good job！Me！

s, t = gets.split.map(&:to_s)
a, b = gets.split.map(&:to_i)
u = gets.to_s.chomp

if s == u
print a - 1
print ' '
print b
else
print a
print ' '
print b - 1
end

#100DaysOfCode 3rd_rap Day: 001/100
I tried AtCoder(A - Serval vs Monster)
I am on 3rd_rap from today.
Rome was not built in a day!!

h, a = gets.split.map(&:to_i)
hp = h / a
if h % a == 0
	puts hp
else
	puts hp + 1
end

#100DaysOfCode 3rd_rap Day: 002/100
I tried AtCoder(A - AC or WA)

n, m = gets.split.map(&:to_i)
puts n <= m ? 'Yes' : 'No'

#100DaysOfCode 3rd_rap Day: 003/100
I studied constant.
Ruby's constants are different from ordinary constants in that they can be reassigned.
Need to be careful when handling them.

COMPUTER = 'MacBookPro'
=> "MacBookPro"

COMPUTER = 'WindowsMachine'
warning: already initialized constant COMPUTER
warning: previous definition of COMPUTER was here
=> "WindowsMachine"

#100DaysOfCode 3rd_rap Day: 004/100
I tried AtCoder(A - Serval vs Monster)
I used next method.

c = gets.to_s.chomp
puts c.next

[String\#next \(Ruby 3\.0\.0 リファレンスマニュアル\)](https://docs.ruby-lang.org/ja/latest/method/String/i/next.html)

#100DaysOfCode 3rd_rap Day: 005/100
I tried AtCoder(A - 500 Yen Coins)

k, x = gets.split.map(&:to_i)
puts 500 * k >= x ? 'Yes' : 'No'

#100DaysOfCode 3rd_rap Day: 006/100
I tried AtCoder(A - Strings)

s, t = gets.split.map(&:to_s)
puts  "#{t}#{s}"

#100DaysOfCode 3rd_rap Day: 007/100
I tried AtCoder(A - Round One)

data = readlines.map { |line| line.chomp.to_i }
puts [1,2,3] - data

https://docs.ruby-lang.org/ja/3.0.0/method/IO/i/readlines.html

#100DaysOfCode 3rd_rap Day: 008/100
I tried AtCoder(A - Blackjack)
I made two patterns.

array = gets.split.map(&:to_i)
sum = 0
array.each {|n| sum += n }
puts sum >= 22 ? 'bust' : 'win'

puts gets.split.map(&:to_i).sum >= 22 ? 'bust' : 'win'

#100DaysOfCode 3rd_rap Day: 009/100
I tried AtCoder(A - Can't Wait for Holiday)
Use case sentence.

day = gets.to_s.chomp
case day
when 'SUN'
puts '7'
when 'MON'
puts '6'
when 'TUE'
puts '5'
when 'WED'
puts '4'
when 'THU'
puts '3'
when 'FRI'
puts '2'
when 'SAT'
puts '1'
end

Use index method.
array = [nil, "SAT", "FRI", "THU", "WED", "TUE", "MON", "SUN"]
puts array.index(gets.chomp)
https://docs.ruby-lang.org/ja/latest/method/String/i/index.html

#100DaysOfCode 3rd_rap Day: 010/100
What is Ynaqdhm? 
I researched 'Ynaqdhm'.
If you see the following display on the command line during execution, you need to take action.

Overwrite /Users/＠＠＠/blog/Gemfile? (enter "h" for help) [Ynaqdhm] h

Y - yes, overwrite ←上書きします。
n - no, do not overwrite ←上書きしません。
a - all, overwrite this and all others←全てを上書き
q - quit, abort←実行の中断
d - diff, show the differences between the old and the new←互換ファイルを
（古いものと、新しいもの）比較する？
h - help, show this help←ヘルプの呼び出し。
m - merge, run merge tool←マージする。ツールの統合をする。

#100DaysOfCode 3rd_rap Day: 011/10
I tried AtCoder(A - Circle)

puts r = gets.to_i ** 2

#100DaysOfCode 3rd_rap Day: 012/100
I tried AtCoder(A - 9x9)

a, b = gets.split.map(&:to_i)
if a > 9 || b > 9
puts -1
else
puts a * b
end

#100DaysOfCode 3rd_rap Day: 013/100
I tried AtCoder(B - log2(N))
I'm going to try B problem at today.

n = gets.to_i

k = 0
x = 2**k
until x > n
	x *= 2
	k += 1
end
puts k - 1

#100DaysOfCode 3rd_rap Day: 014/100
I tried AtCoder(B - How many?)
This is the tweet from yesterday.

s, t = gets.split.map(&:to_i)
count = 0
(0..s).each do |a|
(0..s-a).each do |b|
(0..s-a-b).each do |c|
count += 1 if a * b * c <= t
end
end
end

puts count

#100DaysOfCode 3rd_rap Day: 015/100
I tried AtCoder(B - Booby Prize)

n = gets.to_i
array = gets.split.map(&:to_i)

score = array.sort
booby_score = score[-2]
puts array.find_index(booby_score)+1

[ind\_index\(val\) \-> Integer \| nil\[permalink\]\[rdoc\]\[edit\]
index\(val\) \-> Integer \| nil](https://docs.ruby-lang.org/ja/latest/method/Array/i/find_index.html)

#100DaysOfCode 3rd_rap Day: 016/100
I tried AtCoder(B - Weak Password)

X = gets
X1 = X[0].to_i
X2 = X[1].to_i
X3 = X[2].to_i
X4 = X[3].to_i

array = [X1, X2, X3, X4]

if array.uniq.count == 1
puts "Weak"
elsif  (X1+1).modulo(10) == X2 &&
(X1+2).modulo(10) == X3 &&
(X1+3).modulo(10) == X4
puts "Weak"
else
puts "Strong"
end

#100DaysOfCode 3rd_rap Day: 017/100
I tried AtCoder(B. Cycle Hit)

S = Array.new(4){gets.to_s.chomp}
puts S.uniq.size == 4  ? 'Yes' : 'No'

#100DaysOfCode 3rd_rap Day: 018/100
I tried AtCoder(B - Bouzu Mekuri )

n = gets.chomp.split.map(&:to_i)
s = gets.chomp.chars.map(&:to_i)

c = 0

s.each do |x|
c += 1
if x == 1
if c % 2 == 0
puts "Aoki"
break
else
puts "Takahashi"
break
end
end  
end

#100DaysOfCode 3rd_rap Day: 019/100
I tried AtCoder(B - Can you buy them all?)

N, X = gets.chomp.split.map(&:to_i)
array = gets.split.map(&:to_i)

puts X >= array.sum - N/2 ? 'Yes' : 'No'

#100DaysOfCode 3rd_rap Day: 020/100
I tried AtCoder(B - Factorial Yen Coin)

point = gets.chomp.to_i

sum = 0
div = 2

while point != 0
sum += (point % div)
point /= div
div += 1
end

print sum

#100DaysOfCode 3rd_rap Day: 021/100
I tried AtCoder(	B - Hydrate)

a, b, c, d = gets.chomp.split.map(&:to_i)

if b >= c * d
puts -1
end
1000000.times {|t|
if a + b * t <= c * d * t
@time = t
break
end
}  
puts @time

#100DaysOfCode 3rd_rap Day: 022/100
I tried AtCoder(B - Savings)

n = gets.chomp.to_i

i = 0
money = 0

while money < n do
i += 1
money += i
end

puts i

#100DaysOfCode 3rd_rap Day: 023/100
I tried AtCoder(B - Permutation Check)

n = gets.chomp.to_i
arry_a = gets.split.map(&:to_i).sort

arry_b = []
1.upto(n) do |i|
arry_b << i
end

if arry_a == arry_b
puts 'Yes'
else
puts 'No'
end

#100DaysOfCode 3rd_rap Day: 024/100
I tried AtCoder(B - Nuts)
n = gets.chomp.to_i
arry = gets.split.map(&:to_i)

def nuts(arry)
total = 0
arry.each do |x|
if x > 10
total += (x - 10)
end
end
puts total
end

nuts(arry)

#100DaysOfCode 3rd_rap Day: 025/100
I tried AtCoder(B - AtCoder Condominium)

n, k = gets.split.map(&:to_i)
sum = 0
1.upto(n) do |x|
1.upto(k) do |y|
sum += 100 * x + y
end
end
puts sum

#100DaysOfCode 3rd_rap Day: 026/100
I tried AtCoder(B - 180°)

s = gets.chars.map(&:to_s)
arry = []

s.each do |i|
if i == '6'
arry << '9'
elsif i == '9'
arry << '6'
else
arry << i
end
end

print arry.join.reverse

#100DaysOfCode 3rd_rap Day: 027/100
I tried AtCoder(B - Do you know the second highest mountain?)

n = gets.to_i
name_height = Array.new(n){gets.split}
puts name_height.sort_by{_3.to_i}[-2][0]

#100DaysOfCode 3rd_rap Day: 028/100
I tried AtCoder(B - 200th ABC-200)

n, k = gets.split.map(&:to_i)

k.times do |i|
n % 200 == 0 ? n /= 200 : n = n*1000 + 200
end
puts n

#100DaysOfCode 3rd_rap Day: 029/100
I tried AtCoder(B - Intersection)

n = gets.to_i
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)
x = (b.min) - (a.max)
puts x >= 0 ? x + 1 : 0 

#100DaysOfCode 3rd_rap Day: 030/100
I tried AtCoder(B - Palindrome with leading zeros)
n = gets.chomp.to_s
x = n.gsub(/0+$/, "")

if n == n.reverse
puts "Yes"
elsif x == x.reverse
puts "Yes"
else
puts "No"
end

#100DaysOfCode 3rd_rap Day: 031/100
I tried AtCoder(B - Round Down)

x = gets.chomp.to_s
puts x.to_i.floor

#100DaysOfCode 3rd_rap Day: 032/100
I tried AtCoder(B - Many Oranges)
a,b,w = gets.split.map(&:to_f)
w = w*1000
# 切り上げ floor, 切り捨て cell
if (w/a).floor < (w/b).ceil
puts  "UNSATISFIABLE"
else
puts "#{(w/b).ceil} #{(w/a).floor}"
end

#100DaysOfCode 3rd_rap Day: 033/100
I tried AtCoder(B - Job Assignment)

n = gets.to_i
price = 10**9 + 1
n.times{
a,p,x = gets.split.map(&:to_i)
if a - x < 0
price = [price,p].min
end
}
puts price == 10**9 + 1 ? -1 : price

#100DaysOfCode 3rd_rap Day: 034/100
I tried AtCoder(B - uNrEaDaBlE sTrInG)
s = gets.chomp.to_s

result = "Yes"
for i in 0...(s.size) do
result = "No" if i % 2 == 0 && !/\A[a-z]+\z/.match?(s[i])
result = "No" if i % 2 != 0 && /\A[a-z]+\z/.match?(s[i])
end

puts result

#100DaysOfCode 3rd_rap Day: 035/100
I tried AtCoder(B - Remove It)

n, x = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
a.delete(x)
puts a.join(' ')

#100DaysOfCode 3rd_rap Day: 036/100
I tried AtCoder(A - Weather Forecast)

n = gets.chomp.to_i
s = gets.chars.map(&:to_s)

puts s[n-1] == 'o' ? 'Yes' : 'No'

#100DaysOfCode 3rd_rap Day: 037/100
I tried AtCoder(A - Lexicographic Order)
s, t = gets.split.map(&:to_s)
puts s < t ? 'Yes' : 'No'

I tried AtCoder(B - qwerty)
p = gets.split.map(&:to_i)
arry = ('a'..'z').to_a

puts p.map { |i| arry[i - 1] }.join

#100DaysOfCode 3rd_rap Day: 038/100
I studied Rails application.
I was unclear about the basics, 
so I tried to learn by hand from the beginning.
I'm in the middle of it again, but I'm starting to understand it better.
After all, it is important to learn repeatedly.
https://github.com/shirotamaki/rails_practice_taskleaf

#100DaysOfCode 3rd_rap Day: 039/100
I tried AtCoder(B - AtCoder Quiz)

s = Array.new(3){ gets.to_s.chomp }  
contest = ["ABC", "ARC", "AGC", "AHC"]
puts result = contest - s

#100DaysOfCode 3rd_rap Day: 040/100
I tried AtCoder(B - Billiards)
arry = gets.split.map(&:to_f)
result = arry[0] * arry[3] + arry[2] * arry[1]
puts  result / (arry[1] + arry[3] )

#100DaysOfCode 3rd_rap Day: 041/100
I tried AtCoder(B - Go to Jail)

n = gets.chomp.to_i
d = Array.new(n){ gets.split.map(&:to_i) }

result = d.map { |(x, y)| x == y }
puts result.each_cons(3).any?(&:all?) ? "Yes" : "No"
https://docs.ruby-lang.org/ja/3.0.0/method/Enumerable/i/each_cons.html
https://docs.ruby-lang.org/ja/3.0.0/method/Array/i/any=3f.html

#100DaysOfCode 3rd_rap Day: 042/100
Specification of relationships in models.
The model of a table that contains "foreign keys" always has a belongs_to declaration.
In the intermediate table called Relationship, we have prepared the follower_id followed_id.

belongs_to :follower, class_name: 'User'
belongs_to :followed, class_name: 'User'

has_many :followed_relationships, class_name: 'Relationship', foreign_key: :follower_id
has_many :followed_users, through: :followed_relationships, source: :followed
has_many :follower_relationships, class_name: 'Relationship', foreign_key: :followed_id
has_many :follower_users, through: :follower_relationships, source: :follower

#100DaysOfCode 3rd_rap Day: 043/100
I tried AtCoder(B - Product Max)

a, b, c, d = gets.split.map(&:to_i)
puts [a * c, a * d, b * c, b * d].max

#100DaysOfCode 3rd_rap Day: 044/100
I finally figured out the lauting of rails applications.
So, I've heard it's best to limit Nest to two times.

Rails.application.routes.draw do
mount LetterOpenerWeb::Engine, at: "/letter_opener" if Rails.env.development?
devise_for :users
root to: 'books#index'
resources :books
resources :users, only: %i(index show) do
resources :following, only: %i(index create)
resources :followers, only: :index
end
end

#100DaysOfCode 3rd_rap Day: 045/100
I tried AtCoder(B - Multiple of 9)

n = gets.chomp
arry = n.chars.map(&:to_i)
sum = 0
arry.each { |i| sum += i }

puts sum % 9 == 0 && n.to_i % 9 == 0 ? 'Yes' : 'No'

#100DaysOfCode 3rd_rap Day: 046/100
I wrote blog about module today.
I tried to include the module Effector.

module Effector
def chalk(guitarist)
puts "#{guitarist}: Gyueeeeen!!"
end
end

class Guitar
include Effector
    def play
        chalk('JimiHendrix')
    end
end

#100DaysOfCode 3rd_rap Day: 047/100
I tried AtCoder(	B - Minor Change)

s = gets.chomp.split("")
t = gets.chomp.split("")

cnt = 0
s.size.times do |i|
if s[i] != t[i]
cnt += 1
end
end
puts cnt

#100DaysOfCode 3rd_rap Day: 048/100
I tried AtCoder(B - Mix Juice)

n, k = gets.split.map(&:to_i)
arry = gets.split.map(&:to_i).sort
puts arry[0..(k-1)].sum

#100DaysOfCode 3rd_rap Day: 049/100
I tried AtCoder(B - Crane and Turtle)

x, y = gets.split.map(&:to_i)
if x*2 <= y && y <= x*4 && y.even?
puts 'Yes'
else
puts 'No'
end

#100DaysOfCode 3rd_rap Day: 050/100
I tried AtCoder(B - Crane and Turtle)

n = gets.chomp.to_i
a = gets.split.map(&:to_i)

if a.include?(0)
puts '0'
exit
end

MAX = 1000000000000000000
result = 1
a.each do |i|
result *= i
if result > MAX
puts '-1'
exit
end
end

puts result

#100DaysOfCode 3rd_rap Day: 051/100
I tried AtCoder(B - ... (Triple Dots))

k = gets.chomp.to_i
s = gets.chomp.chars.map(&:to_s)
if s.count <= k
print s.join
else
print s.first(k).join + '... '
end

#100DaysOfCode 3rd_rap Day: 052/100
Today, I'm having trouble with form processing.

<%= form.hidden_field :user_name, :value => @user.name %>
form_with(model: report), which means that I pass @user.name to the user_name column in the report.
@user.name to the user_name column in the report.
https://sakurawi.hateblo.jp/entry/hidden_field

#100DaysOfCode 3rd_rap Day: 053/100
I tried AtCoder(B - Easy Linear Programming)
a, b, c, k = gets.split.map(&:to_i)

if a >= k
puts k
elsif a+b >= k
puts a
else
puts a - (k - (a+b))
end

#100DaysOfCode 3rd_rap Day: 054/100
I tried AtCoder(A - AtCoder Beginner Contest 999)
n = gets.chomp.chars.map(&:to_i)
arry = []
n.each do |i|
if i == 1
arry << 9
else
arry << 1
end
end
puts arry.join

And, I wrote it in one line.

puts gets.chomp.chars.map { |i| i == '1' ? '9' : i == '9' ? '1' : i }.join

#100DaysOfCode 3rd_rap Day: 055/100
I tried AtCoder (B - typo)

s = gets.chomp.chars
t = gets.chomp.chars

if s == t
puts 'Yes'
exit
end

count = s.size
(count-1).times do |i|
if s[i] != t[i]
s[i], s[i+1] = s[i+1], s[i]
break
end
end

if  s == t
puts 'Yes'
else
puts 'No'
end

#100DaysOfCode 3rd_rap Day: 056/100
I tried AtCoder(B - Base K)

K = gets.chomp.to_i
A, B = gets.split.map(&:to_s)
puts A.to_i(K) * B.to_i(K)
https://docs.ruby-lang.org/ja/latest/method/String/i/to_i.html

#100DaysOfCode 3rd_rap Day: 057/100
I tried AtCoder(B - Failing Grade)
N, P = gets.split.map(&:to_i)
arry = gets.split.map(&:to_i)

sum = 0
arry.each do |n|
if n < P
sum += 1
else
# Do nothing
end
end
puts sum  

I wrote it in a different way.One line.
puts arry.count { _1 < P }

#100DaysOfCode 3rd_rap Day: 058/100
I tried AtCoder(B - Go to Jail)
N = gets.chomp.to_i
ary = Array.new(N){ gets.to_s.split.map{ |e| e.to_i } }

result = ary.map { |(x, y)| x == y }
puts result.each_cons(3).any?(&:all?) ? 'Yes' : 'No'

#100DaysOfCode 3rd_rap Day: 059/100
I tried AtCoder(Product Max)
a, b, c, d = gets.split.map(&:to_i)
puts [a * c, a * d, b * c, b * d].max

#100DaysOfCode 3rd_rap Day: 060/100
I tried AtCoder(B - Multiple of 9 )

n = gets.chars.map(&:to_i)
puts n.sum % 9 == 0 ? 'Yes' : 'No'

#100DaysOfCode 3rd_rap Day: 061/100
I tried AtCoder(B - Making Triangle)
n = gets.chomp.to_i
array = gets.chomp.split(' ').map(&:to_i).sort

puts array.combination(3).count { |a, b, c| a < b && b < c && c < a + b }

https://docs.ruby-lang.org/ja/latest/method/Array/i/combination.html

#100DaysOfCode 3rd_rap Day: 062/100
I tried AtCoder(B - Distance)

N, D = gets.split.map(&:to_i)

coordinate = D*D
result = 0
N.times {
x, y = gets.split.map(&:to_i)
result += 1 if x*x + y*y <= coordinate
}
puts result

#100DaysOfCode 3rd_rap Day: 063/100
I tried AtCoder(A - Tires)
I wrote JavaScript.

function main(input) {
input = input.split('\n');
console.log(input[0].endsWith("er") ? "er" : "ist");
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 064/100
I tried AtCoder(A - Exact Price)

function main(input) {
if ( input >= 100 && input % 100 === 0 ) {
console.log("Yes");
} else {
console.log("No");
}
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 065/100
I tried AtCoder(A - Four Digits)

function main(input) {
let array = input.split('\n');
let s = array[0]
let format = 4;
let result = String(s).padStart(format, '0')
console.log(result);
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 066/100
I tried AtCoder(A - Seismic magnitude scales)

const main = (input) => {
const array = input.split(' ')
const magnitude = parseInt(array[0]) - parseInt(array[1])
console.log(32 ** magnitude)
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 067/100
I tried AtCoder(A - AtCoder Quiz 2)

const main = (input) => {
const x = parseInt(input)
if (x < 40) {
console.log(40 - x)
} else if (x < 70) {
console.log(70 - x)
} else if (x < 90) {
console.log(90 - x)
} else if (x >= 90) {
console.log("expert")
}
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 068/100
function main(inputs) {
const lines = inputs.split('\n')
const ary = lines[1].split('')
const day = parseInt(lines[0] -1)
if (ary[day] == 'o') {
console.log('Yes')
} else if ( ary[day] == 'x') {
console.log('No')
}
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 069/100
I tried AtCoder(A - Your First Judge)

function main(input) {
let S = input.split('\n')[0];
if (S === 'Hello,World!') {
console.log('AC')
} else {
console.log('WA')
}
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

This is Conditional (ternary) operator.

function main(input) {
const S = input.split('\n')[0];
const reslut = (S === 'Hello,World!' ?　'AC' : 'WA') 
console.log(result)
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Conditional_Operator

#100DaysOfCode 3rd_rap Day: 070/100
I tried AtCoder(A - New Generation ABC)

function main(input) {
const N = input.split('\n')[0]
const numberOfTimes = parseInt(N)
if (numberOfTimes <= 125) {
console.log('4')
} else if (numberOfTimes <= 211) {
console.log('6')
} else if (numberOfTimes <= 214) {
console.log('8')
}
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

I did learn the if_statement.
![image.png](https://bootcamp.fjord.jp/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBOFJ2QWc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--0f434ca169c8b213eb6c5a760fdb2c223b4adedf/image.png)


#100DaysOfCode 3rd_rap Day: 071/100
I tried AtCoder(A - Libra)

function main(input) {
const arry = input.split(' ')
const left = parseInt(arry[0]) + parseInt(arry[1])
const right = parseInt(arry[2]) + parseInt(arry[3])
if (left == right) {
console.log('Balanced')
} else if (left > right) {
console.log('Left')
} else {
console.log('Right')
}
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 072/100
I tried AtCoder(B - Palindrome with leading zeros)

function main(input) {
const s = input.trim();
const regex = /0+$/;
const result = s.replace(regex, '');
const resultReverse = result.split('').reverse().join('');
if (result === resultReverse) {
console.log('Yes')
} else {
console.log('No')
}
};

main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 073/100
I tried AtCoder(	A - Rotate)

function main(input) {
const s = input.trim();
const arry = Array.from(s)
const arryChange = arry[1] + arry[2] + arry[0]
console.log(arryChange)
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 074/100
I tried AtCoder(B - Round Down)

function main(input) {
const s = input.trim()
const num = s.split(".")
console.log(num[0])
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 075/100
I tried AtCoder(B - Many Oranges)

function main(input) {
const [A, B, W] = input.trim().split(" ").map(Number)
const min = Math.ceil((W * 1000) / B)  //切り上げ
const max = Math.floor((W * 1000) / A) //切り捨て
const ans = max >= min ? `${min} ${max}` : "UNSATISFIABLE"
console.log(ans);
}

main(require("fs").readFileSync("/dev/stdin", "utf8"))

#100DaysOfCode 3rd_rap Day: 076/100
I tried AtCoder(B - Job Assignment)

function main(input) {
input = input.split('\n');
const N = Number(input[0]);
const A = [];
const B = [];
for (let i = 0; i < N; i++) {
const [a,b] = input[i + 1].split(' ').map(Number);
A.push(a);
B.push(b);
}
let ans = 10000000001;
for (let i = 0; i < N; i++) {
for (let j = 0; j < N; j++) {
const tmp = i === j ? A[i] + B[j] : Math.max(A[i], B[j]);
ans = Math.min(ans, tmp);
}
}
console.log(ans);
}

main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 077/100
I tried AtCoder(B - Play Snuke)
function main(line) {
lines = line.split("\n");
const N = Number(lines[0]);
let value = 1000000000;
for (let i = 1; i <= N ; i++) {
let [a, p, x] = lines[i].split(" ").map(Number);
if(x > a){
value = Math.min(value,p);      
}
}
if(value === 1000000000){
console.log(-1);  
}else{
console.log(value);
}
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

#100DaysOfCode 3rd_rap Day: 078/100
I solved the problems in the Udemy JavaScript course.

function calcFactory (val) {
return {
plus: function (target) {
const newVal = val + target
console.log(`${val} + ${target} = ${newVal}`)
val = newVal
},
minus: function (target) {
const newVal = val - target
console.log(`${val} - ${target} = ${newVal}`);
val = newVal
},
multiply: function (target) {
const newVal = val * target
console.log(`${val} * ${target} = ${newVal}`);
val = newVal
},
divide: function (target) {
const newVal = val / target
console.log(`${val} / ${target} = ${newVal}`);
val = newVal
},
}
}

const calc = calcFactory(10)
calc.plus(5)
calc.minus(3)
calc.multiply(3)
calc.divide(2)

#100DaysOfCode 3rd_rap Day: 079/100
It's been a while since I've tweeted about 100DaysOfCode today!
I'd like to tweet using an application released by one of my friend.
Super convenient ! Thank you @yana_gis !!

A - Rotate
const main = (stdin) => {
const s = stdin.trim();
const arry = Array.from(s)
const arryChange = arry[1] + arry[2] + arry[0]
console.log(arryChange)
}
main(require("fs").readFileSync("/dev/stdin", "utf8"));

Users of the 100DayOfCode, Try it !


#100DaysOfCode 3rd_rap Day: 080/100
B - Election
function main(input) {
const args = input.split('\n')
const N = args[0]
const names = args.slice(1, args.length - 1)

counts = {}
let max = 0
let ans
for (let i=0; i<names.length; i++) {
    let key = names[i]
    counts[key] = counts[key] ? counts[key] + 1 : 1
    if(counts[key] > max){
    	max = counts[key]
      	ans = key
    }
}
	console.log(ans)
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'))