# প্যাকেজিং

পাইথনে প্যাকেজিং বলতে বুঝায়, আপনার লেখা বিভিন্ন মডিউল গুলোকে একটা স্ট্যান্ডার্ড ফরম্যাটে একত্র করে বান্ডেল করা যাতে অন্য ইউজাররা খুব সহজেই আপনার বানানো প্রোগ্রামকে ব্যবহার করতে পারে। যেমন ধরুন, ওয়েব থেকে ডাটা স্ক্র্যাপ করার জন্য যাবতীয় সব রকম ফাংশনালিটি গুলো বানিয়ে কিছু ডেভেলপার একটি প্যাকেজ রিলিজ দিয়েছে যার নাম `BeautifulSoup`. আর আমরা খুব সহজেই সেই প্যাকজেটি আমাদের প্রজেক্টে ইন্সটল করে তার বিভিন্ন রেডিমেড ফাংশনকে ব্যবহার করতে পারি।

নিচে আমরা ধাপে ধাপে দেখবো কিভাবে একটি কাস্টম প্যাকেজকে [PyPI](https://pypi.python.org/pypi) তথা Python Package Index -এ আপলোড করতে হয়। ধরে নিচ্ছি, আমাদের প্যাকেজের সোর্স কোড [github](https://github.com) এ হোস্ট করা আছে এবং প্যাকেজটির নাম `mypackage`.

> প্রথমেই, [PyPI Live](http://pypi.python.org/pypi?%3Aaction=register_form) এবং [PyPI Test](http://testpypi.python.org/pypi?%3Aaction=register_form) -এ আপনার একাউন্ট খুলে নিতে পারেন।

`.pypirc` **কনফিগারেশন ফাইল তৈরি**  
এই ফাইলে PyPI এর সাথে আপনার অথেন্টিকেশনের কনফিগারেশন গুলো উল্লেখ থাকবে।

```python
[distutils]
index-servers =
    pypi
    pypitest

[pypi]
repository=https://pypi.python.org/pypi
username=your_username
password=your_password

[pypitest]
repository=https://testpypi.python.org/pypi
username=your_username
password=your_password
```

কাজের সুবিধার জন্য এই ফাইলটিকে আপনার হোম ফোল্ডারে রাখতে পারেন। অর্থাৎ যার লোকেশন হবে `~/.pypirc`

> যেহেতু এই ফাইলে আপনার কিছু সংবেদনশীল তথ্য যেমন পাসওয়ার্ড থাকবে তাই এই ফাইলের পারমিশন বদলে নিতে পারেন - `chmod 600 ~/.pypirc` এই কমান্ড ইস্যু করে।

**প্যাকেজ কন্টেন্ট তৈরি**

ইউজারের জন্য এভাবে প্যাকেজ তৈরি করতে গিয়ে `setuptools` এবং `distutils` মডিউলের দরকার পরে। প্রথমেই একটি ডিরেক্টরির মধ্যে সব গুলো প্রোগ্রাম ফাইলকে রাখতে হবে। ওই একই ডিরেক্টরির মধ্যে `__init__.py` নামের একটি ফাইলও রাখতে হবে। এটা নিয়ম। এর উপস্থিতির মাধ্যমে পাইথন এটাকে একটা প্যাকেজ হিসেবে ধরে নেয়। এই ফাইলটি ফাকাও হতে পারে।

এরপর, আপনার প্রোগ্রাম ফাইলগুলো এবং এই স্পেশাল ইনিসিয়ালাইজার ফাইল সহ ডিরেক্টরিটিকে আরও একটি রুট ডিরেক্টরির মধ্যে রাখতে হবে। এবং সেই রুট ডিরেক্টরির মধ্যে একটি readme ফাইল, একটি লাইসেন্স ফাইল এবং গুরুত্বপূর্ণ একটি ফাইল `setup.py` কে রাখতে হবে।

ডিরেক্টরি লিস্টিং উদাহরণ,

```python
MyPackage/ # Name of this dir can be anything
   LICENSE.txt
   README.md
   setup.py
   setup.cfg
   mypackage/ # actual package name
      __init__.py
      myfile.py
      anotherfile.py
```

`setup.py` ফাইলে কিছু গুরুত্বপূর্ণ তথ্য যুক্ত করতে হয় যাতে করে আপনার ডেভেলপ করা প্যাকেজটি [PyPI](https://pypi.python.org/pypi) তথা Python Package Index এ আপলোড করার উপযোগী হয়। এতে করে ইউজাররা [pip](https://pypi.python.org/pypi/pip) টুল ইউজ করে খুব সহজেই আপনার প্যাকেজটি ইন্সটল করে নিতে পারবে।

ফাইলটি হতে পারে নিচের মত,

```python
from distutils.core import setup

setup(
    name = 'mypackage',
    packages = ['mypackage'], # this must be the same as the name above
    version = '0.1',
    description = 'A random test lib',
    author = 'Nuhil Mehdy',
    author_email = 'nuhil@nuhil.net',
    url = 'https://github.com/nuhil/mypackage', # use the URL to the github repo
    download_url = 'https://github.com/nuhil/mypackage/archive/0.1.tar.gz', # I'll explain this in a second
    keywords = ['testing', 'logging', 'example'], # arbitrary keywords
    classifiers = [],
)
```

`download_url` লিঙ্কের মাধ্যমে আপনার প্যাকেজের টারবল ভার্সন পয়েন্ট করে দিতে হয়। যদি আপনার সোর্স কোড [github](https://github.com/) -এ হোস্ট করা থাকে এবং মুল রিপোজিটরি থেকে একটি ট্যাগ তৈরি করা থাকে তাহলে সেখানে এরকম টারবল রেডি থাকে।

> **ট্যাগ তৈরি করতেঃ** প্রথমে লোকাল রিপোজিটরিতে ঢুকে কমান্ড দিতে হবে `git tag 0.1 -m "Adds a tag so that we can put this on PyPI."` এরপর `git tag` কমান্ড দিয়ে ট্যাগ গুলো দেখা যাবে। আগের কমান্ড দিয়ে ঠিক ঠাক ট্যাগ তৈরি হয়ে থাকলে লিস্ট আসবে এমন - `0.1`. এরপর `git push --tags origin master` কমান্ড দিতে হবে যার মাধ্যমে github এ এই ট্যাগের তথ্য যুক্ত হয়ে যাবে। আর সেই নির্দিষ্ট ট্যাগ ওয়ালা টারবলটী ডাউনলোডের জন্য তৈরি থাকবে এই লিঙ্কে - `https://github.com/{username}/{module_name}/archive/{tag}.tar.gz`

**setup.cfg ফাইল**  
যদি আপনার readme ফাইলটি মার্কডাউন ফরম্যাটে লেখা হয়ে থাকে তাহলে এই ফাইলটি দরকার পরে। এর কন্টেন্ট হবে নিচের মত।

```python
[metadata]
description-file = README.md
```

> `.txt` ফরম্যাটে লেখা readme ফাইল হলে উপরোক্ত ফাইল যুক্ত করার দরকার পরে না।

**PyPI Test এ প্যাকেজ আপলোড**  
প্রথমে নিচের কমান্ড ইস্যু করুন -

```bash
python setup.py register -r pypitest
```

এরপর,

```bash
python setup.py sdist upload -r pypitest
```

সব কিছু ঠিক ঠাক থাকলে আপনার প্যাকেজকে [Test PyPI Repository](https://testpypi.python.org/pypi) তে দেখা যাবে।

**PyPI Live এ প্যাকেজ আপলোড**  
প্রথমে নিচের কমান্ড ইস্যু করুন -

```bash
python setup.py register -r pypi
```

এরপর,

```bash
python setup.py sdist upload -r pypi
```

