## ইনহেরিট্যান্স   

<sub> এই চ্যাপ্টারটি সর্বশেষ হালনাগাদ হয়েছেঃ {{ file.mtime }} সময়ে </sub>   

ইংলিশ শব্দ inheritance এর একটা বাংলা অর্থ হচ্ছে উত্তরাধিকার সূত্রে কিছু পাওয়া। পাইথনে ক্লাস গুলোর মধ্যে কিছু ফাংশনালিটি ও বৈশিষ্ট্য শেয়ার করার একটা পদ্ধতি হচ্ছে ইনহেরিট্যান্স। অর্থাৎ, একটা ক্লাসকে ইনহেরিট (অনুসরণ) করে তার কিছু বৈশিষ্ট্য আরেকটি উত্তরসূরি ক্লাসের মধ্যে নিয়ে আসার ব্যাপারটিকেই ইনহেরিট্যান্স বলা হয়।   

আগের চ্যাপ্টারে আমরা একটা ক্লাস দেখেছি `Monster`. এই ক্লাস থেকে আমরা বিভিন্ন রকম আলাদা আলাদা অবজেক্ট তথা দৈত্য তৈরি করা দেখেছি। একটি ক্লাসে আমরা সেই সব প্রোপার্টি এবং মেথড রাখি যেগুলো এই ক্লাস থেকে বানানো অবজেক্টের কাজে লাগে। কিন্তু যদি এমন হয় যে, `Monster` ক্লাস থেকে বানানো অবজেক্ট গুলোর আরও নিজস্ব কিছু অ্যাক্টিভিটি (মেথড) দরকার যেগুলো আমাদের `Monster` ক্লাস বা টেম্পলেটে নাই। তাহলে কি হবে? আমরা কি তবে ওই ক্লাস থেকে অবজেক্ট বানানো বাদ দিয়ে দেবো? আরেকটি ক্লাস বানিয়ে সেই নতুন ক্লাস থেকে অবজেক্ট তথা একটু ভিন্ন বৈশিষ্ট্যের দৈত্য বানানো শুরু করবো?    

না। বরং আমরা শুধুমাত্র বাড়তি প্রয়োজনীয় ফিচার গুলো নিয়ে একটি ছোট ক্লাস বানাবো ঠিকি কিন্তু কমন বৈশিষ্ট্য গুলোর সুবিধা নেয়ার জন্য সেই `Monster` ক্লাসকেই ইনহেরিট করবো।    

উদাহরণ, 

```python
class Monster:
    def __init__(self, name, color):
        self.name = name
        self.color = color

    def attack(self):
        print('I am attacking...')


class Fogthing(Monster):
    def make_sound(self):
        print('Grrrrrrrrrr\n')


class Mournsnake(Monster):
    def make_sound(self):
        print('Hiiissssshhhh\n')


fogthing = Fogthing("Fogthing", "Yellow")
fogthing.attack()
fogthing.make_sound()

mournsnake = Mournsnake("Mournsnake", "Red")
mournsnake.attack()
mournsnake.make_sound()
```

ধরে নিচ্ছি আমাদের সব দৈত্যই আক্রমণ করে এবং একটা নাম এবং একরকম রং আছে। তাই এসব মিলে আমরা একটি ব্লুপ্রিন্ট (ক্লাস) বানিয়েছি `Monster` নামে। এবার সত্যিকারের দৈত্য অবজেক্ট তৈরির সময় মনে হল যে, `fogthing` আর `mournsnake` দৈত্যের শব্দ তো আলাদা রকম। তখন আমরা বাড়তি এই ফাংশনটা সহ `Fogthing` আর `Mournsnake` নামের দুটো ক্লাস বানিয়ে নিয়েছি কিন্তু সেগুলো মুল `Monster` ক্লাসকে ইনহেরিট করছে। অর্থাৎ নতুন এই দুটি ক্লাসের নিজস্ব কিছু ফিচার আছে সাথে `Monster` ক্লাসের সব ফিচারও পাচ্ছে।   

আউটপুট,

```python
I am attacking...
Grrrrrrrrrr

I am attacking...
Hiiissssshhhh
```

> কোন ক্লাসকে ইনহেরিট করার জন্য ওই ক্লাসের নামটি নতুন ক্লাসের নামের পর ব্র্যাকেটের মধ্যে লিখতে হয়। এখানে `Monster` হচ্ছে সুপারক্লাস আর `Fogthing`, `Mournsnake` হচ্ছে সাবক্লাস


**অভাররাইড**   
যদি সুপারক্লাসের কোন মেথড বা অ্যাট্রিবিউটকে এর একটা সাবক্লাসের মধ্যে আবার ডিফাইন করা হয় তাহলে সেগুলো অভাররাইড হয়ে যায়। যেমন,   

```python
class Monster:
    def __init__(self, name, color):
        self.name = name
        self.color = color

    def attack(self):
        print('I am attacking...')


class Fogthing(Monster):
    def attack(self):
        print('I am killing...')

    def make_sound(self):
        print('Grrrrrrrrrr\n')


fogthing = Fogthing("Fogthing", "Yellow")
fogthing.attack()
fogthing.make_sound()
```

আউটপুট, 

```python
I am killing...
Grrrrrrrrrr
```
উপরের উদাহরণে, `Fogthing` ক্লাস মুল `Monster` ক্লাসের `attack` মেথডকে অভাররাইড করেছে। 

**মাল্টিপল ইনহেরিট্যান্স**   
নিচের প্রোগ্রামটি দেখি এবং অনুমান করি এর আউটপুট কি আসবে, 

```python
class A:
    def where(self):
        print("I am from class A")


class B:
    def where(self):
        print("I am from class B")


class C(A, B):
    pass

an_instance_of_c = C()
an_instance_of_c.where()
```
এখানে, `C` ক্লাসটি `A` এবং `B` দুটো ক্লাসকেই ইনহেরিট করেছে। আবার ওই দুটো ক্লাসের প্রত্যেকটিতেই `where` নামের মেথড আছে। পরিশেষে, যখন `C` ক্লাসের ইন্সট্যান্স তৈরি করে `where` মেথডকে কল করা হচ্ছে তখন আসলে কোন ক্লাসের `where` মেথডটি কল হবে?    
প্রথমেই সেই মেথডকে `C` ক্লাসের মধ্যে খোঁজা হবে, না পেলে `A` ক্লাসের মধ্যে আর সেখানেও না পেলে `B` ক্লাসের মধ্যে খোঁজা হবে। এখন বলা যায় আউটপুট কি আসবে, 

```python
I am from class A
```

এই অর্ডার ভিত্তিক মেথড খোঁজার জন্য পাইথন নিজস্ব নিয়ম ফলো করে এবং সেটা দেখতে চাইলে আমরা প্রোগ্রামে `print(C.mro())` স্টেটমেন্টটি ব্যবহার করতে পারি যার আউটপুট আসবে নিচের মত, 

```python
[<class '__main__.C'>, <class '__main__.A'>, <class '__main__.B'>, <class 'object'>]
```

অর্থাৎ, `C`, `A`, `B`	  

**`super` মেথড**   
ইনহেরিট্যান্স এর ক্ষেত্রে `super`	 একটি গুরুত্বপূর্ণ মেথড। এর মাধ্যমে একটি অবজেক্টের সুপার ক্লাসের মধ্যেকার মেথডকে কল করা যায়। যেমন, 

```python
class A:
    def spam(self):
        print(1)

class B(A):
    def spam(self):
        print(2)
        super().spam()

B().spam()
```

আউটপুট, 

```python
2
1
```


>  সংকলন - [নুহিল মেহেদী](https://nuhil.net)