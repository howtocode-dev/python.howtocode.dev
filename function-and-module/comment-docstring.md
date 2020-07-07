# কমেন্ট ও ডক স্ট্রিং

**কমেন্ট**  
কমেন্ট মানে মন্তব্য। কোড লেখার সময় কোডের সাথে মন্তব্যও লেখা যায়। কিন্তু সেই মন্তব্যের কথা গুলো প্রোগ্রামের মত রান হয় না। তাই এভাবে কোড সাথে কমেন্ট লিখে রাখলে অন্যের সেই কোড বুঝতে সুবিধা হয় এবং ওই কোড দিয়ে কি করা যায় এবং কিভাবে করা যায় সেটাও কোড রান করার আগেই বুঝে নেয়া যায়।

পাইথনে যেকোনো কমেন্ট লাইন লেখার আগে তার আগে `#` \(হ্যাস বা পাউন্ড\) চিহ্ন ব্যবহার করতে হয়। নিচের উদাহরণটি দেখি -

```python
# few variables below
x = 10
y = 5

# make sum of the above two variables
# and store the result in z
z = x + y

print(z) # print the result
# print (x // y)
# another comment
```

উপরের প্রোগ্রামটিতে বেশ কিছু কমেন্ট আমরা লিখেছি যেগুলো পরে বোঝা যাচ্ছে এই প্রোগ্রামে কি করা হয়েছে।

**ডক স্ট্রিং**  
কমেন্টের মত আরও একটি জিনিষ হচ্ছে ডক স্ট্রিং বা ডকুমেন্ট স্ট্রিং। কিন্তু এর ব্যবহার একটু ভিন্ন ভাবে আরও স্পেসিফিক ভাবে করা হয়। সাধারণত মাল্টি লাইন স্ট্রিং কে কোন ফাংশনের মধ্যে শুরুতেই লিখে ওই ফাংশন সম্পর্কিত একটি মন্তব্যের ব্লক লেখা হয় যাকে ডক স্ট্রিং বলা হয়।

```python
def greet(word):
    """
    Print a word with an
    exclamation mark following it.
    """
    print(word + "!")

greet("Hello World")
```

সাধারণ কমেন্ট থেকে এটি একটু আলাদা। যেমন - এই স্ট্রিং গুলোকে প্রোগ্রামের রানটাইমের সময়ও অ্যাক্সেস করা যায় নিচের মত করে,

```python
def greet(word):
    """
    Print a word with an
    exclamation mark following it.
    """
    print(word + "!")

# What the fucntion does?
print(greet.__doc__)

# Make sense, now lets use it    
greet("Hello World")
```

আউটপুট,

```python
    Print a word with an
    exclamation mark following it.

Hello World!
```

উপরের প্রোগ্রামের `print(greet.__doc__)` স্টেটমেন্টটির মাধ্যমে আমরা `greet` ফাংশনের ডকুমেন্টেশন দেখে নিয়েছি এবং তারপর একে কল করে ব্যবহার করেছি।

**স্টাইল গাইড**

[গুগল স্টাইল গাইড](https://github.com/google/styleguide) মোতাবেক খুব সুন্দর ভাবে একটি ফাংশনের ডক স্ট্রিং লেখা যেতে পারে নিচের মত করে,

```python
def square_root(n):
    """Calculate the square root of a number.

    Args:
        n: the number to get the square root of.
    Returns:
        the square root of n.
    Raises:
        TypeError: if n is not a number.
        ValueError: if n is negative.

    """
    pass
```

অর্থাৎ প্রথমেই ফাংশনের কাজ। তারপর তার প্যারামিটার গুলোর বর্ণনা। এরপরে সেই ফাংশনের কোন রিটার্ন ভ্যালু থাকলে তার বর্ণনা। অতঃপর এটি কোন এরর বা এক্সেপশন রেইজ করবে কিনা এ ব্যাপারটা লেখা।

> ভালো প্রোগ্রামার অবশ্যই ভালো কমেন্ট এবং ডক স্ট্রিং লিখে থাকেন। তাড়াহুড়ায় এড়িয়ে যাওয়া একদম উচিৎ নয়।

