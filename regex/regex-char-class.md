# ক্যারেক্টার ক্লাস

ক্যারেক্টার ক্লাস হচ্ছে কিছু ক্যারেক্টারের সমষ্টি বা সেট। এর মাধ্যমে এই সেটের মধ্যেকার যেকোনো একটি ক্যারেক্টারের সাথে নির্দিষ্ট কোন স্ট্রিং -কে ম্যাচ করে দেখা যায়। আবার একটি নির্দিষ্ট রেঞ্জ পর্যন্ত ক্যারেক্টার এর সাথেও ম্যাচ করা যায়। `[]` বন্ধনী ব্যবহার করে এবং এর মধ্যে নির্দিষ্ট কিছু ক্যারেক্টার যুক্ত করে একটি ক্যারেক্টার ক্লাস তৈরি করা হয় যা পরবর্তীতে সার্চ প্যাটার্ন হিসেবে ব্যবহার করা হয়।

উদাহরণ,

**একটি ক্যারেক্টার ম্যাচ**

```python
import re

# A character set containing all vowels
pattern = r"[aeiou]"

# Lets check whether a word got a vowel in it or not
if re.search(pattern, "grey"):
   print("The word 'grey' got at least one vowel!")
else:
   print("No vowel found!")    

if re.search(pattern, "qwertyuiop"):
   print("The word 'qwertyuiop' got at least one vowel!")
else:
   print("No vowel found!")

if re.search(pattern, "rhythm myths"):
   print("The word 'rhythm myths' got at least one vowel!")
else:
   print("No vowel found!")
```

আউটপুট,

```python
The word 'grey' got at least one vowel!
The word 'qwertyuiop' got at least one vowel!
No vowel found!
```

**ক্যারেক্টার রেঞ্জ ম্যাচ**

ক্যারেক্টার সেট তৈরি করার সময় `-` চিহ্ন দিয়ে একটি রেঞ্জ ডিফাইন করা হয়। যেমন, `[a-z]` ক্লাস দিয়ে ছোট হাতের যেকোনো ইংলিশ বর্ণ ম্যাচ করা হয়। `[A-Z]` দিয়ে যেকোনো বড় হাতের ইংলিশ বর্ণ। `[0-9]` দিয়ে যেকোনো নিউমেরিক ডিজিট ম্যাচ করে দেখা হয়, ইত্যাদি।

উদাহরণ,

```python
import re

pattern = r"[A-Z][A-Z][0-9]"

if re.search(pattern, "NS1 is prefix of first name server address."):
   # Found NS1 as match
   print("OK")

if re.search(pattern, "You should put a second one with NS2 as prefix."):
   # Found NS2 as match
   print("OK")

if re.search(pattern, "I don\'t have any nameserver."):
   print("NS3")
else:
   print("Not OK!")

if re.search(pattern, "PY3K"):
   # Found PY3 as match
   print("OK")
```

আউটপুট,

```python
OK
OK
Not OK!
OK
```

অর্থাৎ উপরের `[A-Z][A-Z][0-9]` প্যাটার্নের মাধ্যমে একটি স্ট্রিং এর মধ্যে "দুটি বড় হাতের ইংলিশ বর্ণ এবং তার সাথেই যুক্ত একটি নিউমেরিক ডিজিট" সম্পন্ন একটি প্যাটার্ন ম্যাচ করা হচ্ছে।

**ক্যারেক্টার ক্লাসে ^ এর ব্যবহার**

আমরা আগে জেনেছি যে, `^` হচ্ছে একটি মেটা ক্যারেক্টার। ক্যারেক্টার ক্লাসে `^` এর গুরুত্বপূর্ণ একটি ভূমিকা আছে। এর মাধ্যমে সাধারণ ভাবে তৈরি করা একটি ক্যারেক্টার ক্লাসের ঠিক উল্টো অর্থ ডিফাইন করা হয়। অর্থাৎ এটি একটি ক্যারেক্টার ক্লাসের অর্থকে invert করে ফেলে। অর্থাৎ `[A-Z]` দিয়ে যদি যেকোনো বড় হাতের ইংলিশ বর্ণের উপস্থিতি যাচাই করা হয়, তাহলে `[^A-Z]` দিয়ে যেকোনো বড় হাতের ইংলিশ বর্ণের অনুপস্থিতি যাচাই বা ম্যাচ করা হয়।

উদাহরণ,

```python
import re

# Match string that contains NOT ALL Capital letters
pattern = r"[^A-Z]"

if re.search(pattern, "a sentence with all lower case letters."):
   print("Match 1")

if re.search(pattern, "A sentence with mixed English letters."):
   print("Match 2")

if re.search(pattern, "HEADING"):
   # All Capital letters
   # No Match
   print("Match 3")

if re.search(pattern, "HEADING WITH ALL CAPITAL LETTERS"):
   # All Capital letters 
   # but "spaces" makes it True to NOT ALL Capital
   print("Match 4")
```

আউটপুট,

```python
Match 1
Match 2
Match 4
```

> ক্যারেক্টার ক্লাস ডিফাইন করার সময় `^` মেটা ক্যারেক্টারটির এর ভূমিকা থাকলেও অন্য মেটা ক্যারেক্টার যেমন - `.` বা `$` এর কোন ভূমিকা নেই।

