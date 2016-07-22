## প্রোপার্টিস

কোন একটি মেথডের উপর `property` ডেকোরেটোর ব্যবহার করে প্রোপার্টি ডিফাইন করা হয়। এর একটা বহুল ব্যবহার দেখা যায় কোন ইন্সট্যান্স অ্যাট্রিবিউটকে রিড-অনলি বানানোর ক্ষেত্রে। যখন একটি ইন্সট্যান্স অ্যাট্রিবিউটকে কল করা হয় এবং যদি ওই নামে একটি মেথড থাকে যা কিনা `property` ডেকোরেটোর দিয়ে ডেকোরেট করা, তখন পক্ষান্তরে সেই মেথডটিই কল হয়। আর এভাবেই একটি অ্যাট্রিবিউটকে রিড-অনলি করার একটা রাস্তা পাওয়া যায়। নিচের উদাহরণটি দেখলে আরও পরিষ্কার হয়ে যাবে।    

```python
class Pizza:
    def __init__(self, toppings):
        self.toppings = toppings

    @property
    def pineapple_allowed(self):
        return False

pizza = Pizza(["cheese", "tomato"])
print(pizza.pineapple_allowed)
pizza.pineapple_allowed = True
```

আউটপুট, 

```python
False
Traceback (most recent call last):
  File "/Users/nuhil/Documents/Python/property.py", line 11, in <module>
    pizza.pineapple_allowed = True
AttributeError: can't set attribute
```

<br/>
**`setter/getter`** ফাংশন ব্যবহার করেও প্রোপার্টি ডিফাইন করা যায়। `setter` ফাংশন ব্যবহার করে প্রোপার্টির ভ্যালু সেট করা যায়। আর `getter` ফাংশন ব্যবহার করে ওই প্রোপার্টির ভ্যালু অ্যাক্সেস করা যায়।    
`setter` ডিফাইন করার জন্য প্রোপার্টির নাম এবং একটি ডট চিহ্ন দিয়ে `setter` কিওয়ার্ড লিখে একটি ডেকোরেটর হিসেবে নির্দেশ করতে হয়। `getter` ডিফাইন করার ক্ষেত্রেও একই নিয়ম।   

উদাহরণ, 

<script src="https://gist.github.com/nuhil/ad5e21c37ee4ac3aee5f6517d0d2faff.js"></script>   

উপরের প্রোগ্রামে, প্রথমত ৭ নাম্বার লাইনে `pineapple_allowed` মেথডকে একটি প্রোপার্টি ডিফাইন করা হয়েছে। এতে করে, ২০ নাম্বার লাইনে এই প্রোপার্টির ভ্যালু অ্যাক্সেস করতে গেলে বস্তুত `pineapple_allowed` মেথডটি কল হয় এবং যা পক্ষান্তরে `self._pineapple_allowed = False` এর উপর ভিত্তি করে `False` রিটার্ন করে।    
এরপর, ১০ নাম্বার লাইনে, `@pineapple_allowed.setter` ডেকোরেটর ব্যবহার করে ওই প্রোপার্টির জন্য একটি `setter` মেথড ডিফাইন করা হয়েছে। আর তাই, ২১ নাম্বার লাইনে `pizza.pineapple_allowed = True` স্টেটমেন্ট এক্সিকিউট হবার সময় আসলে `pineapple_allowed` সেটার মেথডটি কল হচ্ছে।  এই মেথডটি ১৫ নাম্বার লাইনে, `_pineapple_allowed` নামের প্রাইভেট ভ্যারিয়েবলের মান বদলে দেয় যার প্রমাণ পাওয়া যায় ২২ নাম্বার লাইনে নতুন করে `print(pizza.pineapple_allowed)` প্রিন্টের মাধ্যমে।   

আউটপুট, 

```python
False
Enter the password: 123456
True
```
