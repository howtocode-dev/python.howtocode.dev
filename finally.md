## ফাইনালি   

যদি এমন দরকার হয় যে, যতই এক্সেপশন তৈরি হোক না কেন কিছু কোডকে রান করানো দরকার, তখন `finally` স্টেটমেন্ট ব্যবহার করা হয়। `try`, `except` ব্লকের নিচে `finally` ব্লক ব্যবহার করতে হয়। `try` বা `except` ব্লকের কোড রান হবার পর এই `finally` ব্লকের মধ্যে থাকা কোড গুলো রান হবেই। একটি উদাহরণ দেখি - 

```python
try:
   print("Hello")
   print(1 / 0)
except ZeroDivisionError:
   print("Divided by zero")
finally:
   print("This code will run no matter what")
```  

আউটপুট, 

```python
Hello
Divided by zero
This code will run no matter what
```   

উপরের প্রোগ্রামে, `try` ব্লকের মধ্যে প্রথম প্রিন্ট স্টেটমেন্টের পর দ্বিতীয় প্রিন্ট স্টেটমেন্টে শূন্য দিয়ে ভাগের চেষ্টার কারনে `ZeroDivisionError` এক্সেপশন তৈরি হচ্ছে। সেটাকে সঠিকভাবে হ্যান্ডেল করায় `except` ব্লকের মধ্যে থাকা `print("Divided by zero")` এক্সিকিউট করছে। এবং পরিশেষে, যেহেতু ঘটনা যাই হোক `finally` ব্লক এর কোড এক্সিকিউট হবেই, তাই `print("This code will run no matter what")` স্টেটমেন্টটিও কাজ করছে।   

যদি `finally` ব্লকের আগে এমন কোন এক্সেপশন তৈরি হয় যাকে সঠিক ভাবে হ্যান্ডেল করা হয় নাই, সে অবস্থাতেও `finally` ব্লকের কোড রান হবে। যেমন -  

```python
try:
   print(1)
   print(10 / 0)
except ZeroDivisionError:
   print(unknown_var)
finally:
   print("This is executed last")
```   

আউটপুট,  

```python
1
This is executed last
Traceback (most recent call last):
  File "/Users/nuhil/Documents/Python/Test.py", line 3, in <module>
    print(10 / 0)
ZeroDivisionError: division by zero

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/Users/nuhil/Documents/Python/Test.py", line 5, in <module>
    print(unknown_var)
NameError: name 'unknown_var' is not defined
```   
উপরের প্রোগ্রামের `try` ব্লকের মধ্যে একটি এক্সেপশন তৈরি হয় এবং সেটা `except` ব্লকে হ্যান্ডেল করা হয়। কিন্তু সেই হ্যান্ডেল করার ব্লকের মধ্যে আবার এমন একটা ভ্যারিয়েবল প্রিন্ট করতে চাওয়া হয়েছে যাকে ডিফাইন করাই হয় নাই। আর তাতে করে সেখানে একটা `NameError` টাইপের এক্সেপশন তৈরি হয় (যদিও এটাকে হ্যান্ডেল করা হয় নি)। তারপরেও `finally` ব্লক কাজ করছে আর তাই `This is executed last` কে আউটপুট স্ক্রিনে দেখা যাচ্ছে।  
   