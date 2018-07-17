## Assertions  

পাইথনে assertion তথা স্যানিটি চেক এনাবেল বা ডিজ্যাবল করে প্রোগ্রাম টেস্টিং এর কাজ করা হয়। কিন্তু, স্যানিটি চেক (sanity-check) আসলে কি? খুব দ্রুত একটি স্টেটমেন্টকে পর্যবেক্ষণ করে সেটার ফলাফলের সত্যতা যাচাই করাকেই স্যানিটি চেক বলা হয়।  

`assert` স্টেটমেন্ট ব্যবহার করে এই কুইক টেস্ট করা হয়। যখন পাইথন কোন প্রোগ্রামের যেকোনো যায়গায় এই `assert` স্টেটমেন্টটি পায় তখন সেটাকে দ্রুত যাচাই করে এবং স্টেটমেন্টটি সত্য হোক সেটা আশা করে। কিন্তু তা না হলে পাইথন `AssertionError` টাইপের এক্সেপশন থ্রো (তৈরি) করে। একটি উদাহরণ দেখি -  

```python
print(1)
assert 2 + 2 == 4
print(2)
assert 1 + 1 == 3
print(3)
```   

আউটপুট, 

```python
1
2
Traceback (most recent call last):
  File "/Users/nuhil/Desktop/Test.py", line 4, in <module>
    assert 1 + 1 == 3
AssertionError
```   

উপরের প্রোগ্রামের প্রথম প্রিন্ট স্টেটমেন্টের পর একটি assertion সেট করা হয়েছে। সেখানে একটি সাধারণ অ্যারিদম্যাটিক কন্ডিশন যাচাই করা হয়েছে `assert` ব্যবহার করে। সেই স্যানিটি চেকটি সত্য বা পাশ হয়েছে (২ আর ২ যোগ করলে ৪ হয়)। তাই, `print(2)` স্টেটমেন্ট কাজ করছে। এরপর আবার একটি স্যানিটি চেক সেট করা হয়েছে। কিন্তু, স্বাভাবিক ভাবেই সেটি সত্য নয় (১ আর ১ যোগ করে ৩ হয় না)। তাই পাইথন সেখানে একটি `AssertionError` এক্সেপশন থ্রো করেছে। আর তাই, এর পরে থাকা `print(3)` স্টেটমেন্টটি এক্সিকিউটও হয় নি।   

সাধারণত প্রোগ্রামারগণ কোন একটি ফাংশনের ডেফিনেশনের শুরুতেই এরকম স্যানিটি চেক ব্যবহার করেন ইনপুট/আর্গুমেন্ট ডাটা চেক করার জন্য। আবার ফাংশন কল এর পরেও ব্যবহার করে থাকেন ফাংশনের আউটপুট ডাটা চেক করার জন্য।

আরেকটি উদাহরণ,  

```python
def KelvinToFahrenheit(Temperature):
   assert (Temperature >= 0),"Colder than absolute zero!"
   return ((Temperature-273)*1.8)+32

print(KelvinToFahrenheit(273))
print(int(KelvinToFahrenheit(505.78)))
print(KelvinToFahrenheit(-5))
```   

আউটপুট,  

```python
32.0
451
Traceback (most recent call last):
  File "/Users/nuhil/Desktop/Test.py", line 7, in <module>
    print KelvinToFahrenheit(-5)
  File "/Users/nuhil/Desktop/Test.py", line 2, in KelvinToFahrenheit
    assert (Temperature >= 0),"Colder than absolute zero!"
AssertionError: Colder than absolute zero!
```  
> বলা বাহুল্য, অন্যান্য এক্সেপশনের মত এই এক্সেপশনকেও `try`, `except` দিয়ে হ্যান্ডেল করা যায়। 

