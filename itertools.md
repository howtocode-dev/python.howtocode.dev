# itertools   

<sub> এই চ্যাপ্টারটি সর্বশেষ হালনাগাদ হয়েছেঃ {{ file.mtime }} সময়ে </sub>

এটি পাইথনের একটি স্ট্যান্ডার্ড মডিউল যার বেশ কিছু ফাংশন ব্যবহৃত হয় ফাংশনাল প্রোগ্রামিং এর সময়। যেমন,   
`count` ফাংশন একটি নির্দিষ্ট ভ্যালু থেকে ইনফিনিট পর্যন্ত হিসাব করে।   
`cycle` ফাংশন একটি iterable কে ইনফিনিট পর্যন্ত ইটারেট করে।    
`repeat` ফাংশন ইনিফিনিট অথবা একটি নির্দিষ্ট পরিমাণ পর্যন্ত একটি অবজেক্টকে রিপিট করে।    

উদাহরণ,

```python
from itertools import count

for i in count(3):
    print(i)
    if i >= 11:
        break
```

আউটপুট,

```python
3
4
5
6
7
8
9
10
11
```

[ম্যাপ ও ফিল্টার](http://python.howtocode.com.bd/map-filter.html) যেমন কোন ইটারেবল এর উপর কাজ করে তেমনি itertools এর বেশ কিছু ফাংশন যেকোনো রকম iterable যেমন লিস্ট, ডিকশনারি এর উপর কাজ করতে সাহায্য করে। যেমন `accumulate` ফাংশনের মাধ্যমে একটি লিস্টের সব গুলো ভ্যালুর রানিং টোটাল পাওয়া সম্ভব।

উদাহরণ,

```python
from itertools import accumulate

my_numbers = [1, 2, 3, 4, 5, 6]
accumulated_numbers = accumulate(my_numbers)
list_of_accu_nums = list(accumulated_numbers)
print(list_of_accu_nums)
```

আউটপুট,

```python
[1, 3, 6, 10, 15, 21]
```

আরেকটি মজার ফাংশন `takewhile` যার নাম শুনেই বোঝা যাচ্ছে এটা কিছু সময় পর্যন্ত কিছু একটা নিয়ে নেয়। আর আগেই বলা হয়েছে এর অপারেশন হতে পারে যেকোনো ইটারেবলের উপর। এটা সেই সব ভ্যালুকে বের করে নেয় যেগুলোর জন্য একটি নির্দিষ্ট প্রেডিকেট সত্য হয়। নিচের উদাহরণে `lambda x: x <= 6` ল্যাম্বডাটি একটি প্রেডিকেট। ল্যাম্বডা নিয়ে পড়তে হবে [এখানে](http://python.howtocode.com.bd/lambda.html)

উদাহরণ, 

```python
from itertools import takewhile

my_numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
nums_less_equal_six = takewhile(lambda x: x <= 6, my_numbers)
filtered_numbers = list(nums_less_equal_six)
print(filtered_numbers)
```

আউটপুট, 

```python
[1, 2, 3, 4, 5, 6]
```

আরও ফাংশন এবং উদাহরণ, 

```python
from itertools import product, permutations

letters = ("A", "B")
print(list(product(letters, range(2))))
print(list(permutations(letters))) 
```

আউটপুট, 

```python
[('A', 0), ('A', 1), ('B', 0), ('B', 1)]
[('A', 'B'), ('B', 'A')]
```

>  সংকলন - [নুহিল মেহেদী](https://nuhil.net)

