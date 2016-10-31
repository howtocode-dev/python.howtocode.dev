# লিস্ট কম্প্রিহেনশন

আমরা এই চ্যাপ্টারে লিস্ট কম্প্রিহেনশন সম্পর্কে জানার চেষ্টা করব। লিস্ট কম্প্রিহেনশন বিষয়টা বোঝার জন্য একটা উদাহরণ দিয়ে দেখা যাক।

ধরি, `num_list` একটি পাইথন লিস্ট যেখানে ১-১০ সংখ্যাগুলো আছে।

```python
num_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

এখন আপনাকে যদি বলা হয় পাইথনে একটি কোড লিখতে যেটা কিনা সংখ্যাগুলো থেকে শুধু জোড় সংখ্যাগুলো নিয়ে আরেকটি লিস্ট তৈরি করতে এবং আপনার যদি লিস্ট কম্প্রিহেনশন সম্পর্কে ধারণা না থাকে তাহলে আপনি অবশ্যই এভাবে লিখবেন,

```python
even_num_list = []
for num in num_list:
	if num % 2 == 0:
        even_num_list.append(num)
print (even_num_list)
```

#### আউটপুট

```python
[2, 4, 6, 8, 10]
```

কিন্তু আপনার যদি এ ব্যাপারে ভাল ধারণা থাকে তাহলে আপনি কোডটি এক লাইনেই লিখতে পারবেন।

```python
even_num_list = [even_num for even_num in num_list if even_num % 2 == 0]
print (even_num_list)
```

চমৎকার, তাই না?

এটাই পাইথনের মজা, প্রতিটা ল্যাঙ্গুয়েজের আলাদা কিছু বৈশিষ্ট্য থাকে যেটা তাকে আলাদা করে তোলে। লিস্ট কম্প্রিহেনশন পাইথনের ক্ষেত্রে এরকম অন্যতম একটি বৈশিষ্ট্য।

কিন্তু এটা করলাম কীভাবে? একটু ভিজুয়ালাইজ করার চেষ্টা করি!

![listcomprehension_gif](http://i.imgur.com/Yj9qlEw.gif)

## লিস্ট কম্প্রিহেনশন কী?

একটা লিস্ট / ইটার‍্যাবল থেকে আরেকটা লিস্টে রূপান্তর করার একটা পদ্ধতি। 

পাইথনের লিস্ট কম্প্রিহেনশন জিনিসটা বেশ মজার কিন্তু একই সাথে পাইথন বিগিনার দের জন্য একটু ঝামেলাকর। সেটা দূর করার জন্যই এই চ্যাপ্টার।

## রিড্যাবিলিটি

অনেকসময় অন্যের করা লিস্ট কম্প্রিহেনশনের কোডগুলো বোঝা কঠিন হয়ে যায়। সেক্ষেত্রে আপনি চাইলে ভেঙ্গেও লিখতে পারেন।

```python
even_num_list = [
  num
  for num in num_list
  if num % 2 == 0
]

print(even_num_list)
```

চলুন আরও কিছু উদাহরণ দেখা যাক।

### নেস্টেড লুপের লিস্ট কম্প্রিহেনশন

নেস্টেড লুপের লিস্ট কম্প্রিহেনশন দেখানোর জন্য 2D ম্যাট্রিক্সের উদাহরণ দেখানোর উপরে কিছু নাই। মনে করুন, আপনার একটা  Matrix / 2D Array আছে, সেটাকে আপনি ফ্ল্যাটেন বা 1D করতে চাচ্ছেন, এই সমস্যাটা আমরা এভাবে সমাধান করতে পারি,

```python
matrix_1d = []
matrix_2d = [[1, 2, 3],
			[4, 5, 6]]

for row in matrix_2d:
    for num in row:
        matrix_1d.append(num)
print(matrix_1d)
```

#### আউটপুট

```
[1, 2, 3, 4, 5, 6]
```

লিস্ট কম্প্রিহেনশন ব্যবহার করে,

```python
matrix_2d = [[1, 2, 3],
			[4, 5, 6]]

matrix_1d = [num for row in matrix_2d for num in row]
```

#### আউটপুট

```
[1, 2, 3, 4, 5, 6]
```

আগের মতই কপি পেস্ট করলাম, প্রথমে যেটা অ্যাড করব সেটা লিখলাম তারপর টপ লেভেল লুপ এবং অবশেষে নেস্টেড লুপ লিখে কোডটি কম্প্লিট করলাম।

ধরুন, আপনি `matrix_1d` তে প্রতিটা এলিমেন্টের বর্গ বা স্কয়ার ভ্যালু নিতে চাচ্ছেন, তাহলে কোড হবে এমন,

```python
matrix_1d = [num**2 for row in matrix_2d for num in row]
```

#### আউটপুট

```
[1, 4, 9, 16, 25, 36]
```

### বাক্য থেকে Vowel দূর করা 

সাধারণ নিয়মে,

```python
vowels = 'aeiou'
sentence = 'I am awesome!'
filtered_letters = []

for letter in sentence:
	if letter not in vowels:
		filtered_letters.append(letter)
		
print(''.join(filtered_letters))
```

#### আউটপুট

```python
In [5]: print(''.join(filtered_letters))
I m wsm!
```

**লিস্ট কম্প্রিহেনশন ব্যবহার করে**

```python
In [23]: vowels = 'aeiou'

In [24]: sentence = 'I am awesome'

In [25]: filtered_sentence = ''.join([letter for letter in sentence if letter not in vowels])

In [26]: filtered_sentence
Out[26]: 'I m wsm'
```


### ডিকশনারি কম্প্রিহেনশন

আমরা যদি দুইটা লিস্ট থেকে একটা ডিকশনারি বানাতে চাই, যেখানে প্রথমটি `Key` এবং পরেরটি `Value` তাহলে সাধারণ নিয়মে এভাবে কোড লিখব,

```python
fruit_ranking = [1, 2, 3]
fruit_name = ['Mango', 'Pineapple', 'Watermelon']
fruit_rank_dict = {}

for i in range(len(fruit_ranking)):
	fruit_rank_dict[fruit_ranking[i]] = fruit_name[i]
	
print(fruit_rank_dict)
```

#### আউটপুট 

```
 {1: 'Mango', 2: 'Pineapple', 3: 'Watermelon'}
```

**লিস্ট কম্প্রিহেনশন** ব্যবহার করে,

```python
In [32]: fruit_ranking = [1, 2, 3]

In [33]: fruit = ['Mango', 'Pineapple', 'Watermelon']

In [34]: fruit_ranking_dict = { fruit_ranking[i] : fruit[i] for i in range(len(fruit_ranking)) }

In [35]: fruit_ranking_dict
Out[35]: {1: 'Mango', 2: 'Pineapple', 3: 'Watermelon'}
```

কোন কোন ক্ষেত্রে লিস্ট কম্প্রিহেনশন ব্যবহার করা শুধু সুবিধাজনক তা-ই নয়, সিম্পল এক্সপ্রেশনে এটা ফর লুপের চেয়েও ফাস্ট। কম্পলেক্স এক্সপ্রেশনে ফর লুপ আর লিস্ট কম্প্রিহেনশনের পারফর্মেন্স প্রায় একই। 
