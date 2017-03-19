## গ্রুপ্স    
রেগুলার এক্সপ্রেশনের একটি নির্দিষ্ট অংশকে বন্ধনীর মধ্যে আবদ্ধ করে একটি গ্রুপ তৈরি করা হয়। 

উদাহরণ,   
```python
import re

pattern = r"egg(spam)*"

if re.match(pattern, "egg"):
    print("Match 1")

if re.match(pattern, "eggspamspamspamegg"):
    print("Match 2")

if re.match(pattern, "spam"):
    print("Match 3")
```  
উপড়ে `(spam)` একটি গ্রুপ। অর্থাৎ উপরোক্ত প্যাটার্নটি এই প্রকাশ করে যে - স্ট্রিং এর শুরুতে egg থাকবে এবং এর পর এক বা একাধিক spam ওয়ার্ড থাকবে অথবা নাও থাকতে পারে (* দিয়ে প্রকাশ করা হয়েছে)।    

আউটপুট,  

```python
Match 1
Match 2
```

গ্রুপের ম্যাচ করা কন্টেন্ট গুলকে group() ফাংশনের সাহায্যে অ্যাক্সেস করা যায়। যেমন, group() বা group(0) ব্যবহার করে পুরো ম্যাচটি অ্যাক্সেস করা যেতে পারে। নিচের মত করে, 

উদাহরণ,   

```python
import re

pattern = r"a(bc)(de)(f(g)h)i"

match = re.match(pattern, "abcdefghijklmnop")
if match:
    print(match.group())
    print(match.group(0))
    print(match.group(1))
    print(match.group(2))
    print(match.groups())
```   

আউটপুট,  

```python
abcdefghi
abcdefghi
bc
de
('bc', 'de', 'fgh', 'g')
```   

**স্পেশাল গ্রুপ**  

অনেক রকম স্পেশাল গ্রুপের মধ্যে named group এবং non-capturing group অন্যতম।  

named group এর ফরম্যাট দেখতে `(?P<name>...)` -এ রকম। যেখানে name হচ্ছে গ্রুপটির নাম এবং ... হচ্ছে কন্টেন্ট। এর আচরণ অন্যান্য নরমাল গ্রুপের মতই, শুধুমাত্র যেহেতু এর একটি নাম আছে তাই একে অ্যাক্সেস করার জন্য group(name) অর্থাৎ নাম ব্যবহার করা যায়। যদিও সাথে সাথে নাম্বারও ব্যবহার করা যেতে পারে।   
অন্যদিকে, non-capturing group এর ফরম্যাট দেখতে (?: ...) -এ রকম এবং গ্রুপ ফাংশন ব্যবহার করে একে অ্যাক্সেস করা যায় না।   

উদাহরণ,  

```python
import re

pattern = r"(?P<first>abc)(?:def)(ghi)"

match = re.match(pattern, "abcdefghi")
if match:
    print(match.group("first"))
    print(match.groups())
```   

আউটপুট, 

```python
abc
('abc', 'ghi')
```  

**আরও একটি মেটাক্যারেক্টার**   
`|` অর্থাৎ অথবা প্রকাশক একটি মেটা ক্যারেক্টার মাঝে মাঝে খুবি উপকারী। এটা অনেক লজিক্যাল OR অপারেটর এর মত। নিচের উদাহরণ দেখলে আরও পরিষ্কার হয়ে যাবে,  

```python
import re

pattern = r"gr(a|e)y"

match = re.match(pattern, "gray")
if match:
    print ("Gray is fine!")

match = re.match(pattern, "grey")
if match:
    print ("Grey is OK also!")    

match = re.match(pattern, "griy")
if match:
    print ("No way, what Griy is?!!")
```   

অর্থাৎ, প্যাটার্নটি এরকম - প্রথমে gr থাকবে, এরপর হয় a অথবা e থাকবে এবং শেষে y থাকবে। এরকম একটি ম্যাচ খুঁজবে এই প্যাটার্নটি। আর তাই উপড়ের প্রোগ্রামের আউটপুট আসবে নিচের মত,  

```python
Gray is fine!
Grey is OK also!
```   
