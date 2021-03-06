# পরিচিতি

পাইথনে রেগুলার এক্সপ্রেশন নিয়ে কাজ করার জন্য বিল্ট ইন মডিউল হিসেবে আছে `re` নামের মডিউল। রেগুলার এক্সপ্রেশন ব্যবহারের সময় প্যাটার্ন খোঁজার জন্য যে স্পেশাল এক্সপ্রেশন বা সহজ করে বলতে সার্চ টার্ম ডিফাইন করতে হয় সেটা সাধারণত `r"expression"` এভাবে ডিফাইন করতে হয়। `r` দিয়ে Raw স্ট্রিং বোঝানো হয়। অর্থাৎ এর মধ্যে কোন রকম ক্যারেক্টার এক্সকেইপ করা হয় না যা রেগুলার এক্সপ্রেশনের ব্যবহারকে আরও ইফসিয়েন্ট করে তোলে।

প্রথমেই একটি উদাহরণ দেখি -

```python
import re

pattern = r"Bangla"

result = re.match(pattern, "Bangladesh")

if result:
    print("Match Found!")
else:
    print("No match")
```

আউটপুট,

```python
Match Found!
```

প্রথমেই `re` মডিউলকে import করে নেয়া হয়েছে যাতে করে এর মধ্যেকার সব ফাংশনকে সহজে আমাদের প্রোগ্রামে ব্যবহার করতে পারি। এরপর একটি ভ্যারিয়েবলে Raw ফরম্যাটে Bangla স্ট্রিং টিকে স্টোর করা হয়েছে। বস্তুত এই প্যাটার্নটিকেই আমরা একটু পরে আরেকটি স্ট্রিং এর মধ্যে খুঁজব। এরপর `re` এর `match` ফাংশন কে কল করা হয়েছে এবং এর দুটো আর্গুমেন্ট পাঠিয়ে দেয়া হয়েছে - একটি হচ্ছে কি ম্যাচ করে দেখতে চাই, আরেকটি হচ্ছে কোথায় ম্যাচ করে দেখতে চাই। `match` ফাংশন একটি স্ট্রিং এর শুরুতে ডিফাইন করা প্যাটার্নকে খুঁজে দেখে।

এই অপারেশনটির রেজাল্ট ষ্টোর করা হয়েছে `result` ভ্যারিয়েবলে। সাধারণত, নির্দিষ্ট প্যাটার্ন ম্যাচ পাওয়া গেলে এখানে একটি ম্যাচ সম্বলিত অবজেক্ট পাওয়া যাবে আর ম্যাচ পাওয়া না গেলে None রিটার্ন আসবে। এরপরের if-else এর কাজ টুকু সবাই বুঝতে পারছেন আশা করি।

এরকম আরও মজার সব ফাংশন আছে `re` মডিউলে। যেমন - `search`, `findall`, `finditer` ইত্যাদি। আমরা নিচে একটি প্রোগ্রামের মধ্যেই সব গুলোর ব্যবহার দেখবো এবং তারপর বিশ্লেষণ করবো।

```python
import re

pattern = r"Bangladesh"

if re.search(pattern, "There is country named Bangladesh in south asia!"):
    print("Match Found!")
else:
    print("No match")

pattern = r"bangla"    
print(re.findall(pattern, "Bangladeshi bangla and indian bangla are differnet."))
```

আউটপুট,

```python
Match Found!
['bangla', 'bangla']
```

`search` ফাংশন এর মাধ্যমে একটি প্যাটার্নকে একটি স্ট্রিং এর যেকোনো যায়গায় খুঁজে দেখা হয়। `match` এর মত শুধু শুরুতে চেক করার মত নয়। `findall` ফাংশনও `search` এর মত সব যায়গায় ম্যাচ খুঁজে দেখে এবং খুঁজে পাওয়া সব গুলো ম্যাচকে একটি লিস্ট হিসেবে রিটার্ন করে। উপরের প্রোগ্রামে এই দুটি ফাংশনের ব্যবহারকেই দেখানো হয়েছে।

**রিটার্ন অবজেক্টের কিছু মেথড**  
আগেও একবার বলা হয়েছে যে - রেগুলার এক্সপ্রেশন সম্বলিত একটি স্টেটমেন্ট বা অপারেশন একটি অবজেক্ট রিটার্ন করে। এই রিটার্ন করা অবজেক্টের আবার অনেক গুলো সুবিধাজনক মেথড থাকে যেগুলো ব্যবহার করে আরও কিছু গুরুত্বপূর্ণ কাজ সম্পন্ন করা যায়। যেমন - `group`, `start`, `end`, `span` ইত্যাদি।

উদাহরণ,

```python
import re

pattern = r"bin"

match = re.search(pattern, "combination")
if match:
    print(match.group())
    print(match.start())
    print(match.end())
    print(match.span())
```

আউটপুট,

```python
bin
3
6
(3, 6)
```

`group` মেথড রিটার্ন করছে ম্যাচ হয়ে যাওয়া সাব স্ট্রিং টিকে। `start`, `end` দিয়ে স্ট্রিং এর মধ্যে হওয়া ম্যাচ এর শুরু আর শেষের ইনডেক্স বা অবস্থান জানা যায়। `span` এর মাধ্যমে এই ইনডেক্স দুটিকে একটি টাপল হিসেবে রিটার্ন পাওয়া যায়।

> সংকলন - [নুহিল মেহেদী](https://nuhil.net)

