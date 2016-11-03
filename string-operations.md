## স্ট্রিং অপারেশনস

**কনক্যাটেনেশন**   

ইন্টিজার বা ফ্লটের মত, স্ট্রিংকেও যোগ করা যায় যাকে কনক্যাটেনেশন বলা হয়।    

```python
>>> "Spam" + 'eggs'
'Spameggs'
```   

```python
>>> print("First string" + ", " + "second string")
First string, second string
```

তাই বলে কোন নাম্বারের সাথে স্ট্রিং যোগ করা যাবে না,    

```python
>>> "2" + "2"
'22'
>>> 1 + '2' + 3 + '4'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```   

যোগের মত স্ট্রিং নিয়ে গুনও করা যায়। তবে এই গুন হতে হবে একটি স্ট্রিং এর সাথে একটি ইন্টিজার নাম্বারের। স্ট্রিং এবং স্ট্রিং এর মধ্যে নয় অথবা ফ্লট টাইপের ডাটার সাথে নয়।   

উদাহরণ,   

```python
>>> print("spam" * 3)
spamspamspam

>>> 4 * '2'
'2222'

>>> '17' * '87'
TypeError: can't multiply sequence by non-int of type 'str'

>>> 'pythonisfun' * 7.0
TypeError: can't multiply sequence by non-int of type 'float'
```   

**স্ট্রিং ফরম্যাটিং**   
নন স্ট্রিং ডাটার সাথে স্ট্রিং টাইপের ডাটাকে যুক্ত করে সুন্দর স্ট্রিং আউটপুট তৈরি করতে `format` মেথড ব্যবহার করা হয়। এর মাধ্যমে একটি স্ট্রিং এর মধ্যে থাকা কিছু আর্গুমেন্টকে রিপ্লেস বা সাবস্টিটিউট করা যায়। `format` মেথডের মধ্যের প্রত্যেকটি আর্গুমেন্ট দিয়ে এর সামনে থাকা স্ট্রিং এর মধ্যের প্লেস হোল্ডার গুলোকে রিপ্লেস করা হয়। প্লেস হোল্ডার গুলো `{}` এর সাথে ইনডেক্স বা নাম ব্যবহার করে ডিফাইন করা হয়। একটি উদাহরণ দেখলেই বিষয়টি পরিষ্কার হয়ে যাবে - 

```python
scores = {"PHP": 6, "Python": 6.5, "Java": 5, "Swift": 6}
msg = "My self score on PHP: {0}, Python: {1}, Java: {2}, Swift: {3}". format(scores["PHP"], scores["Python"], scores["Java"], scores["Swift"])

print(msg)
```  

আউটপুট, 

```python
My self score on PHP: 6, Python: 6.5, Java: 5, Swift: 6
```   

`format` মেথডের মধ্যে নাম ওয়ালা আর্গুমেন্ট পাঠিয়ে এবং স্ট্রি ং এর মধ্যের প্লেস হোল্ডার গুলোতে সেই নামে সেগুলোকে ব্যবহার করেও উপরের মত আউটপুট আনা যায় -  

```pyhton
values = [20, 300, 60, 12]
message = "If x = {x} and y = {y}, then x+y = {z}".format(x = 20, y = 300, z = 20+300)

print(message)
```   

আউটপুট,  

```python
If x = 20 and y = 300, then x+y = 320
```   

**কিছু গুরুত্বপূর্ণ ফাংশন**   
নিচে স্ট্রিং নিয়ে কাজ করার জন্য বেশ কিছু গুরুত্বপূর্ণ এবং উপকারী ফাংশনের উদাহরণ দেয়া হল - 

```python
print(", ".join(["apple", "orange", "pineapple"]))
#prints "apple, orange, pineapple"

print("Hello ME".replace("ME", "world"))
#prints "Hello world"

print("This is a sentence.".startswith("This"))
# prints "True"

print("This is a sentence.".endswith("sentence."))
# prints "True"

print("This is a sentence.".upper())
# prints "THIS IS A SENTENCE."

print("AN ALL CAPS SENTENCE".lower())
#prints "an all caps sentence"

print("a, e, i, o, u".split(", "))
#prints "['a', 'e', 'i', 'o', 'u']"
```  

`join` মেথড একটি স্ট্রি ং ওয়ালা লিস্টের স্ট্রি ং গুলোকে একত্রিত করে কিন্তু মাঝে খানে নির্ধারিত একটি সেপারেটর ব্যবহার করে। যেমন উপরের উদাহরণে,  `apple`, `orange`, `pineapple` এই তিনটি ভ্যালুকে একত্রিত করা হয়েছে কিন্তু তাদের মধ্যে কমা `,` সেপারেটর ব্যবহার করে।  

`replace` মেথডের মাধ্যমে একটি সাব স্ট্রি ং কে খুঁজে সেখানে অন্য কিছু রিপ্লেস করা যায়। যেমন উপরের উদাহরণে - `ME` রিপ্লেস করে `world` বসানো হয়েছে।   

`startswith`, `endswith` মেথডের মাধ্যমে কোন একটি ব্যাক্যর শুরু বা শেষ নির্দিষ্ট কোন সাবস্ট্রি ং দিয়ে হয়েছে কিনা তা চেক করা যায়। `upper` এবং `lower` মেথডের কাজ না বললেও সবাই বুঝে নিয়েছেন আশা করা যায়।  

`split` মেথড হচ্ছে `join` মেথডের উল্টো। অর্থাৎ একটি বাক্যেকে নির্দিষ্ট কোন সেপারেটর এর সাপেক্ষে ভেঙ্গে একটি লিস্ট তৈরি করা যায় এই মেথডের মাধ্যমে। সেটাই দেখানো হয়েছে উপরের উদাহরণের শেষ প্রিন্ট স্টেটমেন্টে।  