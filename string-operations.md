## স্ট্রিং অপারেশনস

**কনক্যাটেনেশন (Concatenation)**   

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

**রিপিটেশন (Repetition)**

যোগের মত স্ট্রিং নিয়ে গুনও করা যায়, একে রিপিটেশন বলে। তবে এই গুন হতে হবে একটি স্ট্রিং এর সাথে একটি ইন্টিজার নাম্বারের। স্ট্রিং এবং স্ট্রিং এর মধ্যে নয় অথবা ফ্লট টাইপের ডাটার সাথে নয়।   

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
msg = "My self score on PHP: {0}, Python: {1}, Java: {2}, Swift: {3}". format(6, 6.5, 5, 6)

print(msg)
```  

আউটপুট,

```python
My self score on PHP: 6, Python: 6.5, Java: 5, Swift: 6
```   

ফরম্যাটিংয়ের সময় ইন্ডেক্সগুলো 0, 1, 2.... এইভাবে সিরিয়ালি দিতে হবে ব্যাপারটা কিন্তু এমন না। ইচ্ছে করলেই এগুলো আগে পরে কিংবা একাধিকবার করেও দেয়া যায়।

```
>>> '{2}, {1}, {0}'.format('a', 'b', 'c')
'c, b, a'
>>> '{0}{1}{0}'.format('abra', 'cad')
'abracadabra'
```

`format` মেথডের মধ্যে নাম ওয়ালা আর্গুমেন্ট পাঠিয়ে এবং স্ট্রিং এর মধ্যের প্লেস হোল্ডার গুলোতে সেই নামে সেগুলোকে ব্যবহার করেও কাজ করা যায় -  

```python
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
```
`join` মেথড একটি স্ট্রিং ওয়ালা লিস্টের (লিস্ট নিয়ে পরবর্তীতে আলোচনা করা হয়েছে) স্ট্রিং গুলোকে একত্রিত করে কিন্তু মাঝখানে নির্ধারিত একটি সেপারেটর ব্যবহার করে। যেমন উপরের উদাহরণে,  `apple`, `orange`, `pineapple` এই তিনটি ভ্যালুকে একত্রিত করা হয়েছে কিন্তু তাদের মধ্যে কমা `,` সেপারেটর ব্যবহার করে।  

```python
print("Hello ME".replace("ME", "world"))
#prints "Hello world"
```
`replace` মেথডের মাধ্যমে একটি সাব স্ট্রিং কে খুঁজে সেখানে অন্য কিছু রিপ্লেস করা যায়। যেমন উপরের উদাহরণে - `ME` রিপ্লেস করে `world` বসানো হয়েছে।

```python
print("This is a sentence.".startswith("This"))
# prints "True"

print("This is a sentence.".endswith("sentence."))
# prints "True"
```
`startswith`, `endswith` মেথডের মাধ্যমে কোন একটি ব্যাক্যর শুরু বা শেষ নির্দিষ্ট কোন সাবস্ট্রিং দিয়ে হয়েছে কিনা তা চেক করা যায়।

```python
print("This is a sentence.".upper())
# prints "THIS IS A SENTENCE."

print("AN ALL CAPS SENTENCE".lower())
#prints "an all caps sentence"
```
`upper()` মেথড স্ট্রিংয়ের সবগুলো ক্যারেক্টারকে `uppercase` এ পরিবর্তিত করে। একইভাবে `lower()` মেথড ট্রিংয়ের সবগুলো ক্যারেক্টারকে `lowercase` এ পরিবর্তিত করে।

```python
print("a, e, i, o, u".split(", "))
#prints "['a', 'e', 'i', 'o', 'u']"
```  


`split` মেথড হচ্ছে `join` মেথডের উল্টো। অর্থাৎ একটি বাক্যেকে নির্দিষ্ট কোন সেপারেটর এর সাপেক্ষে ভেঙ্গে একটি লিস্ট তৈরি করা যায় এই মেথডের মাধ্যমে। সেটাই দেখানো হয়েছে উপরের উদাহরণে।
