## এক্সেপশন রেইজ (তৈরি) করা  

আগে আমরা দেখেছি কিভাবে পাইথন প্রয়োজনে নিজে থেকেই প্রোগ্রামে কিছু এক্সেপশন তৈরি করে। চাইলে ম্যানুয়ালি কোড লিখেও প্রোগ্রামের নির্দিষ্ট কোন যায়গায় এক্সেপশন রেইজ বা সহজ ভাবে বলতে গেলে এক্সেপশন তৈরি করা যায়। `raise` স্টেটমেন্ট ব্যবহার করে এভাবে কাস্টম এক্সেপশন তৈরি করা যায়। নিচের উদাহরণটি দেখি - 

```python
print("Hello")
raise NameError('HiThere')
```  

আউটপুট, 

```python
Hello
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: HiThere
```  

উপরের প্রোগ্রামের দ্বিতীয় লাইনে আমরা ম্যানুয়ালি একটি `NameError` টাইপের এক্সেপশন তৈরি করেছি যার কারনে পাইথন সাধারণভাবেই সেই এক্সেপশনটি থ্রো করেছে। 

উপরের মত এক্সেপশনের আর্গুমেন্ট (HiThere) সেট না করেও শুধু `NameError` এক্সপশন থ্রো করে যেত। যেমন নিচের মত - 

```python
raise TypeError
```  

আউটপুট, 

```python
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError
```  

`raise` এর একটি মজার ব্যবহার দেখবো নিচের উদাহরণে,   

```python
try:
	num = 5 / 0
except:
	print("Custom message about an error!")
	raise
```  

আউটপুট, 

```python
Custom message about an error!
Traceback (most recent call last):
  File "/Users/nuhil/Desktop/Test.py", line 2, in <module>
    num = 5 / 0
ZeroDivisionError: integer division or modulo by zero
```   

খেয়াল করুন কি ঘটছে উপরের প্রোগ্রামে। খুব সহজেই বোঝা যাচ্ছে যে `try` ব্লকে একটি এক্সেপশন ঘটছে। এটাও বুঝতে পারছি যে সেটা `ZeroDivisionError` এক্সেপশন হতে পারে কারন শূন্য দিয়ে ৫ কে ভাগ করার চেষ্টা করা হয়েছে। কিন্তু আমরা `except` ব্লকে নির্দিষ্ট করে কোন এক্সেপশন ডিফাইন করে সেটা হ্যান্ডেল করছি না। তারপরেও শেষ নাগাদ পাইথন আমাদেরকে `ZeroDivisionError: integer division or modulo by zero` এক্সেপশন দেখাতে পারছে। এর কারন - আমরা `except` এর মধ্যে `raise` ব্যবহার করেছি। এভাবেও `raise` কে কাজে লাগিয়ে এর আগে ঘটে যাওয়া এক্সেপশনের টাইপ পেয়ে যেতে পারি।   



