# এক্সেপশন

এটি এমন একটি ইভেন্ট যা ঘটে তখনই, যখন একটি প্রোগ্রামের স্বাভাবিক এক্সিকিউশনের মধ্যে কোন বাধার উৎপত্তি হয়। অর্থাৎ যখন একটি পাইথন স্ক্রিপ্ট এমন কোন একটি সমস্যাপূর্ণ অবস্থার সম্মুখীন হয় যা সে এড়িয়ে যেতে পারে না অথবা সমাধান করতে পারে না অতঃপর প্রোগ্রামের এক্সিকিউশন বন্ধ হয়ে যায় - সেরকম ঘটনাকে এক্সেপশন বলা হয়। এক্সেপশন এর আভিধানিক অর্থ থেকেও বোঝা যায় যে ব্যতিক্রম কোন অবস্থার উৎপত্তি।

সাধারণত ভুল কোড বা ইনপুটের জন্য প্রোগ্রামের মধ্যে এক্সেপশন তৈরি হয় যা সঠিকভাবে হ্যান্ডেল না করলে প্রোগ্রাম অনাকাঙ্ক্ষিত ভাবে বন্ধ হয়ে যেতে পারে। একটি উদাহরণ দিয়ে আমারা বোঝার চেষ্টা করি -

```python
a = 2500
b = 0

print(a/b)
print("I did it")
```

আউটপুট,

```python
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```

উপরের প্রোগ্রামে, গণিতের নিয়ম অনুযায়ী `a` কে `b` দিয়ে ভাগ করা সম্ভব না আর তাই যখনই `print(a/b)` স্টেটমেন্টটি এক্সিকিউট হতে চেয়েছে তখনি এক ধরণের ব্যতিক্রম অবস্থার উৎপত্তি হয়েছে যাকে এক্সেপশন বলা হচ্ছে। আর তাই পাইথন ওই প্রোগ্রামের পরবর্তী স্টেটমেন্ট গুলো এক্সিকিউট না করে বরং প্রোগ্রাম এক্সিকিউশন বন্ধ করে দিয়েছে। কিন্তু দেখা যাচ্ছে কোডের লেখায় বা নিয়মে কিন্তু কোন ভুল নাই। শুধুমাত্র রান টাইমেই এই পরিস্থিতি তৈরি হয়েছে। তাই এরকম অবস্থায় পাইথন এক্সেপশন তৈরি করে।

প্রোগ্রামের মধ্যে বিভিন্ন কারনে বিভিন্ন রকম exception তৈরি হয়। কিছু কিছু নির্দিষ্ট কারণের জন্য ঘটা অনাকাঙ্ক্ষিত অবস্থা গুলোর সাপেক্ষে পাইথনে অনেক এক্সেপশন আছে। নিচে কয়েকটি উল্লেখ করা হলঃ

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>&#x98F;&#x995;&#x9CD;&#x9B8;&#x9C7;&#x9AA;&#x9B6;&#x9A8;&#x9C7;&#x9B0; &#x9A8;&#x9BE;&#x9AE;</b>
      </th>
      <th style="text-align:left"><b>&#x9AC;&#x9B0;&#x9CD;&#x9A3;&#x9A8;&#x9BE;</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Exception</td>
      <td style="text-align:left">&#x9B8;&#x9AC; &#x9B0;&#x995;&#x9AE; &#x98F;&#x995;&#x9CD;&#x9B8;&#x9C7;&#x9AA;&#x9B6;&#x9A8;&#x9C7;&#x9B0;
        &#x9AC;&#x9C7;&#x99C; &#x995;&#x9CD;&#x9B2;&#x9BE;&#x9B8;</td>
    </tr>
    <tr>
      <td style="text-align:left">StopIteration</td>
      <td style="text-align:left">&#x9AF;&#x996;&#x9A8; &#x98F;&#x995;&#x99F;&#x9BF; &#x987;&#x99F;&#x9BE;&#x9B0;&#x9C7;&#x99F;&#x9B0;&#x9C7;&#x9B0;
        next() &#x9AE;&#x9C7;&#x9A5;&#x9A1;&#x99F;&#x9BF; &#x995;&#x9CB;&#x9A8;
        &#x985;&#x9AC;&#x99C;&#x9C7;&#x995;&#x9CD;&#x99F;&#x995;&#x9C7; &#x9AA;&#x9DF;&#x9C7;&#x9A8;&#x9CD;&#x99F;
        &#x995;&#x9B0;&#x9C7; &#x9A8;&#x9BE;</td>
    </tr>
    <tr>
      <td style="text-align:left">ArithmeticError</td>
      <td style="text-align:left">&#x9A8;&#x9BF;&#x989;&#x9AE;&#x9C7;&#x9B0;&#x9BF;&#x995; &#x995;&#x9CD;&#x9AF;&#x9BE;&#x9B2;&#x995;&#x9C1;&#x9B2;&#x9C7;&#x9B6;&#x9A8;&#x9C7;&#x9B0;
        &#x99C;&#x9A8;&#x9CD;&#x9AF; &#x9A4;&#x9C8;&#x9B0;&#x9BF; &#x9B9;&#x9DF;
        &#x98F;&#x9AE;&#x9A8; &#x98F;&#x995;&#x9CD;&#x9B8;&#x9C7;&#x9AA;&#x9B6;&#x9A8;&#x9C7;&#x9B0;
        &#x9AC;&#x9C7;&#x99C; &#x995;&#x9CD;&#x9B2;&#x9BE;&#x9B8;</td>
    </tr>
    <tr>
      <td style="text-align:left">OverflowError</td>
      <td style="text-align:left">&#x9AF;&#x996;&#x9A8; &#x98F;&#x995;&#x99F;&#x9BF; &#x9A8;&#x9BF;&#x989;&#x9AE;&#x9C7;&#x9B0;&#x9BF;&#x995;
        &#x99F;&#x9BE;&#x987;&#x9AA;&#x9C7;&#x9B0; &#x9AE;&#x9CD;&#x9AF;&#x9BE;&#x995;&#x9CD;&#x9B8;&#x9BF;&#x9AE;&#x9BE;&#x9AE;
        &#x9B2;&#x9BF;&#x9AE;&#x9BF;&#x99F; &#x985;&#x9A4;&#x9BF;&#x995;&#x9CD;&#x9B0;&#x9AE;
        &#x995;&#x9B0;&#x9C7;</td>
    </tr>
    <tr>
      <td style="text-align:left">ZeroDivisonError</td>
      <td style="text-align:left">&#x9AF;&#x996;&#x9A8; &#x9B6;&#x9C2;&#x9A8;&#x9CD;&#x9AF; &#x9A6;&#x9BF;&#x9DF;&#x9C7;
        &#x9AD;&#x9BE;&#x997;&#x9C7;&#x9B0; &#x998;&#x99F;&#x9A8;&#x9BE; &#x998;&#x99F;&#x9C7;</td>
    </tr>
    <tr>
      <td style="text-align:left">ImportError</td>
      <td style="text-align:left">&#x9AF;&#x996;&#x9A8; import &#x9B8;&#x9CD;&#x99F;&#x9C7;&#x99F;&#x9AE;&#x9C7;&#x9A8;&#x9CD;&#x99F;
        &#x9AB;&#x9C7;&#x987;&#x9B2; &#x995;&#x9B0;&#x9C7; &#x985;&#x9B0;&#x9CD;&#x9A5;&#x9BE;&#x9CE;
        &#x995;&#x9CB;&#x9A8; &#x995;&#x9BE;&#x9B0;&#x9A8;&#x9C7; import &#x9B8;&#x9AE;&#x9CD;&#x9AA;&#x9A8;&#x9CD;&#x9A8;
        &#x9B9;&#x9DF; &#x9A8;&#x9BE;</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>IndexError</p>
        <p>KeyError</p>
      </td>
      <td style="text-align:left">&#x9AF;&#x996;&#x9A8; &#x98F;&#x995;&#x99F;&#x9BF; &#x9B8;&#x9BF;&#x995;&#x9CB;&#x9DF;&#x9C7;&#x9A8;&#x9CD;&#x9B8;
        &#x99F;&#x9BE;&#x987;&#x9AA; &#x985;&#x9AC;&#x99C;&#x9C7;&#x995;&#x9CD;&#x99F;&#x9C7;
        &#x99A;&#x9BE;&#x9B9;&#x9BF;&#x9A6;&#x9BE; &#x9AE;&#x9CB;&#x9A4;&#x9BE;&#x9AC;&#x9C7;&#x995;
        &#x987;&#x9A8;&#x9A1;&#x9C7;&#x995;&#x9CD;&#x9B8; &#x9AA;&#x9BE;&#x993;&#x9DF;&#x9BE;
        &#x9AF;&#x9BE;&#x9DF; &#x9A8;&#x9BE;</td>
    </tr>
    <tr>
      <td style="text-align:left">NameError</td>
      <td style="text-align:left">&#x9AF;&#x996;&#x9A8; &#x9A8;&#x9BF;&#x9B0;&#x9CD;&#x9A6;&#x9BF;&#x9B7;&#x9CD;&#x99F;
        &#x9A8;&#x9BE;&#x9AE;&#x9C7;&#x9B0; &#x995;&#x9CB;&#x9A8; &#x986;&#x987;&#x9A1;&#x9C7;&#x9A8;&#x9CD;&#x99F;&#x9BF;&#x9AB;&#x9BE;&#x9DF;&#x9BE;&#x9B0;&#x995;&#x9C7;
        &#x9B2;&#x9CB;&#x995;&#x9BE;&#x9B2; &#x9AC;&#x9BE; &#x997;&#x9CD;&#x9B2;&#x9CB;&#x9AC;&#x9BE;&#x9B2;
        &#x9B8;&#x9CD;&#x995;&#x9CB;&#x9AA;&#x9C7; &#x996;&#x9C1;&#x981;&#x99C;&#x9C7;
        &#x9AA;&#x9BE;&#x993;&#x9DF;&#x9BE; &#x9AF;&#x9BE;&#x9DF; &#x9A8;&#x9BE;</td>
    </tr>
    <tr>
      <td style="text-align:left">IOError</td>
      <td style="text-align:left">&#x9AF;&#x996;&#x9A8; &#x987;&#x9A8;&#x9AA;&#x9C1;&#x99F; &#x9AC;&#x9BE;
        &#x986;&#x989;&#x99F;&#x9AA;&#x9C1;&#x99F; &#x9B8;&#x9AE;&#x9CD;&#x9AA;&#x9B0;&#x9CD;&#x995;&#x9BF;&#x9A4;
        &#x995;&#x9CB;&#x9A8; &#x985;&#x9AA;&#x9BE;&#x9B0;&#x9C7;&#x9B6;&#x9A8;
        &#x9B8;&#x9AB;&#x9B2; &#x9B9;&#x9DF; &#x9A8;&#x9BE; &#x9AF;&#x9C7;&#x9AE;&#x9A8;
        &#x9AB;&#x9BE;&#x987;&#x9B2; &#x9A5;&#x9C7;&#x995;&#x9C7; &#x9AA;&#x9DC;&#x9BE;&#x9B0;
        &#x99C;&#x9A8;&#x9CD;&#x9AF; &#x993;&#x9AA;&#x9C7;&#x9A8; &#x9AB;&#x9BE;&#x982;&#x9B6;&#x9A8;
        &#x995;&#x9BE;&#x99C; &#x995;&#x9B0;&#x9A4;&#x9C7; &#x9A8;&#x9BE; &#x9AA;&#x9BE;&#x9B0;&#x9B2;&#x9C7;</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>SyntaxError</p>
        <p>IndentationError</p>
      </td>
      <td style="text-align:left">&#x9AA;&#x9BE;&#x987;&#x9A5;&#x9A8; &#x9AA;&#x9CD;&#x9B0;&#x9CB;&#x997;&#x9CD;&#x9B0;&#x9BE;&#x9AE;
        &#x9B2;&#x9C7;&#x996;&#x9BE;&#x9B0; &#x9B8;&#x9AE;&#x9DF; &#x9AD;&#x9C1;&#x9B2;
        &#x995;&#x9CB;&#x9A8; &#x995;&#x9BF;-&#x993;&#x9DF;&#x9BE;&#x9B0;&#x9CD;&#x9A1;
        &#x9AC;&#x9BE; &#x9B8;&#x9CD;&#x99F;&#x9C7;&#x99F;&#x9AE;&#x9C7;&#x9A8;&#x9CD;&#x99F;
        &#x9A5;&#x9BE;&#x995;&#x9B2;&#x9C7;</td>
    </tr>
    <tr>
      <td style="text-align:left">RuntimeError</td>
      <td style="text-align:left">&#x9AF;&#x996;&#x9A8; &#x995;&#x9CB;&#x9A8; &#x98F;&#x995;&#x99F;&#x9BF;
        &#x98F;&#x995;&#x9CD;&#x9B8;&#x9C7;&#x9AA;&#x9B6;&#x9A8; &#x998;&#x99F;&#x9C7;
        &#x9AF;&#x9BE; &#x9AA;&#x9BE;&#x987;&#x9A5;&#x9A8;&#x9C7;&#x9B0; &#x9A8;&#x9BF;&#x9B0;&#x9CD;&#x9A6;&#x9BF;&#x9B7;&#x9CD;&#x99F;
        &#x995;&#x9CB;&#x9A8; &#x995;&#x9CD;&#x9AF;&#x9BE;&#x99F;&#x9BE;&#x997;&#x9B0;&#x9BF;&#x9B0;
        &#x98F;&#x995;&#x9CD;&#x9B8;&#x9C7;&#x9AA;&#x9B6;&#x9A8;&#x9C7;&#x9B0;
        &#x9AE;&#x9A7;&#x9CD;&#x9AF;&#x9C7;&#x987; &#x9AA;&#x9B0;&#x9C7; &#x9A8;&#x9BE;</td>
    </tr>
  </tbody>
</table>

