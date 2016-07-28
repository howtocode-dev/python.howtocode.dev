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
