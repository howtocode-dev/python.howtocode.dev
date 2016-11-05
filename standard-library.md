## স্ট্যান্ডার্ড লাইব্রেরী  

তিন ধরণের মডিউল হতে পারে। কিছু মডিউল যেগুলো পাইথনের সাথে বিল্ট-ইন আছে, কিছু আছে যেগুলো অন্য কোন ডেভেলপের তৈরি করেছে, এবং কিছু হতে পারে আপনার নিজের তৈরি। প্রথম ধরণের মডিউলকে বলা হয় স্ট্যান্ডার্ড লাইব্রেরী। অনেক অনেক এরকম লাইব্রেরীর মধ্যে কিছু হচ্ছে -  `string`, `re`, `datetime`, `math`, `random`, `os`, `multiprocessing`, `subprocess`, `socket`, `email`, `json`, `doctest`, `unittest`, `pdb`, `argparse` এবং `sys` যেগুলোর মাধ্যমে খুব সহজেই স্ট্রিং পারসিং, ডাটা সিরিয়ালাইজেশন, টেস্টিং, ডিবাগিং, ডেট টাইম নিয়ে কাজ, কমান্ড লাইন আর্গুমেন্ট রিসিভ, ইমেইল পাঠানো ইত্যাদি অনেক অনেক কাজ করা যায়। সত্যি কথা বলতে - পাইথনের এই বিশাল পরিমাণ স্ট্যান্ডার্ড লাইব্রেরীর কালেকশনের জন্যও এটি একটি অন্যতম জনপ্রিয় প্রোগ্রামিং ভাষা।   

মজার ব্যাপার হচ্ছে কিছু কিছু মডিউল পাইথনে লেখা আবার কিছু কিছু মডিউল সি প্রোগ্রামিং ভাষায় লেখা। [এই লিঙ্কে](https://docs.python.org/3/library/) গেলে পাইথনের স্ট্যান্ডার্ড লাইব্রেরী গুলো সম্পর্কে আরও বিস্তারিত জানা যাবে। আপনাদের সুবিধার্থে লিঙ্ক সহ সেগুলোর লিস্ট নিচেও দেয়া হলঃ    

<div class="toctree-wrapper compound">
<ul>
<li class="toctree-l1"><a class="reference internal" href="intro.html">1. Introduction</a></li>
<li class="toctree-l1"><a class="reference internal" href="functions.html">2. Built-in Functions</a></li>
<li class="toctree-l1"><a class="reference internal" href="constants.html">3. Built-in Constants</a><ul>
<li class="toctree-l2"><a class="reference internal" href="constants.html#constants-added-by-the-site-module">3.1. Constants added by the <code class="docutils literal"><span class="pre">site</span></code> module</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="stdtypes.html">4. Built-in Types</a><ul>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#truth-value-testing">4.1. Truth Value Testing</a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#boolean-operations-and-or-not">4.2. Boolean Operations — <code class="docutils literal"><span class="pre">and</span></code>, <code class="docutils literal"><span class="pre">or</span></code>, <code class="docutils literal"><span class="pre">not</span></code></a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#comparisons">4.3. Comparisons</a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#numeric-types-int-float-complex">4.4. Numeric Types — <code class="docutils literal"><span class="pre">int</span></code>, <code class="docutils literal"><span class="pre">float</span></code>, <code class="docutils literal"><span class="pre">complex</span></code></a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#iterator-types">4.5. Iterator Types</a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#sequence-types-list-tuple-range">4.6. Sequence Types — <code class="docutils literal"><span class="pre">list</span></code>, <code class="docutils literal"><span class="pre">tuple</span></code>, <code class="docutils literal"><span class="pre">range</span></code></a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#text-sequence-type-str">4.7. Text Sequence Type — <code class="docutils literal"><span class="pre">str</span></code></a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#binary-sequence-types-bytes-bytearray-memoryview">4.8. Binary Sequence Types — <code class="docutils literal"><span class="pre">bytes</span></code>, <code class="docutils literal"><span class="pre">bytearray</span></code>, <code class="docutils literal"><span class="pre">memoryview</span></code></a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#set-types-set-frozenset">4.9. Set Types — <code class="docutils literal"><span class="pre">set</span></code>, <code class="docutils literal"><span class="pre">frozenset</span></code></a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#mapping-types-dict">4.10. Mapping Types — <code class="docutils literal"><span class="pre">dict</span></code></a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#context-manager-types">4.11. Context Manager Types</a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#other-built-in-types">4.12. Other Built-in Types</a></li>
<li class="toctree-l2"><a class="reference internal" href="stdtypes.html#special-attributes">4.13. Special Attributes</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="exceptions.html">5. Built-in Exceptions</a><ul>
<li class="toctree-l2"><a class="reference internal" href="exceptions.html#base-classes">5.1. Base classes</a></li>
<li class="toctree-l2"><a class="reference internal" href="exceptions.html#concrete-exceptions">5.2. Concrete exceptions</a></li>
<li class="toctree-l2"><a class="reference internal" href="exceptions.html#warnings">5.3. Warnings</a></li>
<li class="toctree-l2"><a class="reference internal" href="exceptions.html#exception-hierarchy">5.4. Exception hierarchy</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="text.html">6. Text Processing Services</a><ul>
<li class="toctree-l2"><a class="reference internal" href="string.html">6.1. <code class="docutils literal"><span class="pre">string</span></code> — Common string operations</a></li>
<li class="toctree-l2"><a class="reference internal" href="re.html">6.2. <code class="docutils literal"><span class="pre">re</span></code> — Regular expression operations</a></li>
<li class="toctree-l2"><a class="reference internal" href="difflib.html">6.3. <code class="docutils literal"><span class="pre">difflib</span></code> — Helpers for computing deltas</a></li>
<li class="toctree-l2"><a class="reference internal" href="textwrap.html">6.4. <code class="docutils literal"><span class="pre">textwrap</span></code> — Text wrapping and filling</a></li>
<li class="toctree-l2"><a class="reference internal" href="unicodedata.html">6.5. <code class="docutils literal"><span class="pre">unicodedata</span></code> — Unicode Database</a></li>
<li class="toctree-l2"><a class="reference internal" href="stringprep.html">6.6. <code class="docutils literal"><span class="pre">stringprep</span></code> — Internet String Preparation</a></li>
<li class="toctree-l2"><a class="reference internal" href="readline.html">6.7. <code class="docutils literal"><span class="pre">readline</span></code> — GNU readline interface</a></li>
<li class="toctree-l2"><a class="reference internal" href="rlcompleter.html">6.8. <code class="docutils literal"><span class="pre">rlcompleter</span></code> — Completion function for GNU readline</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="binary.html">7. Binary Data Services</a><ul>
<li class="toctree-l2"><a class="reference internal" href="struct.html">7.1. <code class="docutils literal"><span class="pre">struct</span></code> — Interpret bytes as packed binary data</a></li>
<li class="toctree-l2"><a class="reference internal" href="codecs.html">7.2. <code class="docutils literal"><span class="pre">codecs</span></code> — Codec registry and base classes</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="datatypes.html">8. Data Types</a><ul>
<li class="toctree-l2"><a class="reference internal" href="datetime.html">8.1. <code class="docutils literal"><span class="pre">datetime</span></code> — Basic date and time types</a></li>
<li class="toctree-l2"><a class="reference internal" href="calendar.html">8.2. <code class="docutils literal"><span class="pre">calendar</span></code> — General calendar-related functions</a></li>
<li class="toctree-l2"><a class="reference internal" href="collections.html">8.3. <code class="docutils literal"><span class="pre">collections</span></code> — Container datatypes</a></li>
<li class="toctree-l2"><a class="reference internal" href="collections.abc.html">8.4. <code class="docutils literal"><span class="pre">collections.abc</span></code> — Abstract Base Classes for Containers</a></li>
<li class="toctree-l2"><a class="reference internal" href="heapq.html">8.5. <code class="docutils literal"><span class="pre">heapq</span></code> — Heap queue algorithm</a></li>
<li class="toctree-l2"><a class="reference internal" href="bisect.html">8.6. <code class="docutils literal"><span class="pre">bisect</span></code> — Array bisection algorithm</a></li>
<li class="toctree-l2"><a class="reference internal" href="array.html">8.7. <code class="docutils literal"><span class="pre">array</span></code> — Efficient arrays of numeric values</a></li>
<li class="toctree-l2"><a class="reference internal" href="weakref.html">8.8. <code class="docutils literal"><span class="pre">weakref</span></code> — Weak references</a></li>
<li class="toctree-l2"><a class="reference internal" href="types.html">8.9. <code class="docutils literal"><span class="pre">types</span></code> — Dynamic type creation and names for built-in types</a></li>
<li class="toctree-l2"><a class="reference internal" href="copy.html">8.10. <code class="docutils literal"><span class="pre">copy</span></code> — Shallow and deep copy operations</a></li>
<li class="toctree-l2"><a class="reference internal" href="pprint.html">8.11. <code class="docutils literal"><span class="pre">pprint</span></code> — Data pretty printer</a></li>
<li class="toctree-l2"><a class="reference internal" href="reprlib.html">8.12. <code class="docutils literal"><span class="pre">reprlib</span></code> — Alternate <code class="docutils literal"><span class="pre">repr()</span></code> implementation</a></li>
<li class="toctree-l2"><a class="reference internal" href="enum.html">8.13. <code class="docutils literal"><span class="pre">enum</span></code> — Support for enumerations</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="numeric.html">9. Numeric and Mathematical Modules</a><ul>
<li class="toctree-l2"><a class="reference internal" href="numbers.html">9.1. <code class="docutils literal"><span class="pre">numbers</span></code> — Numeric abstract base classes</a></li>
<li class="toctree-l2"><a class="reference internal" href="math.html">9.2. <code class="docutils literal"><span class="pre">math</span></code> — Mathematical functions</a></li>
<li class="toctree-l2"><a class="reference internal" href="cmath.html">9.3. <code class="docutils literal"><span class="pre">cmath</span></code> — Mathematical functions for complex numbers</a></li>
<li class="toctree-l2"><a class="reference internal" href="decimal.html">9.4. <code class="docutils literal"><span class="pre">decimal</span></code> — Decimal fixed point and floating point arithmetic</a></li>
<li class="toctree-l2"><a class="reference internal" href="fractions.html">9.5. <code class="docutils literal"><span class="pre">fractions</span></code> — Rational numbers</a></li>
<li class="toctree-l2"><a class="reference internal" href="random.html">9.6. <code class="docutils literal"><span class="pre">random</span></code> — Generate pseudo-random numbers</a></li>
<li class="toctree-l2"><a class="reference internal" href="statistics.html">9.7. <code class="docutils literal"><span class="pre">statistics</span></code> — Mathematical statistics functions</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="functional.html">10. Functional Programming Modules</a><ul>
<li class="toctree-l2"><a class="reference internal" href="itertools.html">10.1. <code class="docutils literal"><span class="pre">itertools</span></code> — Functions creating iterators for efficient looping</a></li>
<li class="toctree-l2"><a class="reference internal" href="functools.html">10.2. <code class="docutils literal"><span class="pre">functools</span></code> — Higher-order functions and operations on callable objects</a></li>
<li class="toctree-l2"><a class="reference internal" href="operator.html">10.3. <code class="docutils literal"><span class="pre">operator</span></code> — Standard operators as functions</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="filesys.html">11. File and Directory Access</a><ul>
<li class="toctree-l2"><a class="reference internal" href="pathlib.html">11.1. <code class="docutils literal"><span class="pre">pathlib</span></code> — Object-oriented filesystem paths</a></li>
<li class="toctree-l2"><a class="reference internal" href="os.path.html">11.2. <code class="docutils literal"><span class="pre">os.path</span></code> — Common pathname manipulations</a></li>
<li class="toctree-l2"><a class="reference internal" href="fileinput.html">11.3. <code class="docutils literal"><span class="pre">fileinput</span></code> — Iterate over lines from multiple input streams</a></li>
<li class="toctree-l2"><a class="reference internal" href="stat.html">11.4. <code class="docutils literal"><span class="pre">stat</span></code> — Interpreting <code class="docutils literal"><span class="pre">stat()</span></code> results</a></li>
<li class="toctree-l2"><a class="reference internal" href="filecmp.html">11.5. <code class="docutils literal"><span class="pre">filecmp</span></code> — File and Directory Comparisons</a></li>
<li class="toctree-l2"><a class="reference internal" href="tempfile.html">11.6. <code class="docutils literal"><span class="pre">tempfile</span></code> — Generate temporary files and directories</a></li>
<li class="toctree-l2"><a class="reference internal" href="glob.html">11.7. <code class="docutils literal"><span class="pre">glob</span></code> — Unix style pathname pattern expansion</a></li>
<li class="toctree-l2"><a class="reference internal" href="fnmatch.html">11.8. <code class="docutils literal"><span class="pre">fnmatch</span></code> — Unix filename pattern matching</a></li>
<li class="toctree-l2"><a class="reference internal" href="linecache.html">11.9. <code class="docutils literal"><span class="pre">linecache</span></code> — Random access to text lines</a></li>
<li class="toctree-l2"><a class="reference internal" href="shutil.html">11.10. <code class="docutils literal"><span class="pre">shutil</span></code> — High-level file operations</a></li>
<li class="toctree-l2"><a class="reference internal" href="macpath.html">11.11. <code class="docutils literal"><span class="pre">macpath</span></code> — Mac OS 9 path manipulation functions</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="persistence.html">12. Data Persistence</a><ul>
<li class="toctree-l2"><a class="reference internal" href="pickle.html">12.1. <code class="docutils literal"><span class="pre">pickle</span></code> — Python object serialization</a></li>
<li class="toctree-l2"><a class="reference internal" href="copyreg.html">12.2. <code class="docutils literal"><span class="pre">copyreg</span></code> — Register <code class="docutils literal"><span class="pre">pickle</span></code> support functions</a></li>
<li class="toctree-l2"><a class="reference internal" href="shelve.html">12.3. <code class="docutils literal"><span class="pre">shelve</span></code> — Python object persistence</a></li>
<li class="toctree-l2"><a class="reference internal" href="marshal.html">12.4. <code class="docutils literal"><span class="pre">marshal</span></code> — Internal Python object serialization</a></li>
<li class="toctree-l2"><a class="reference internal" href="dbm.html">12.5. <code class="docutils literal"><span class="pre">dbm</span></code> — Interfaces to Unix “databases”</a></li>
<li class="toctree-l2"><a class="reference internal" href="sqlite3.html">12.6. <code class="docutils literal"><span class="pre">sqlite3</span></code> — DB-API 2.0 interface for SQLite databases</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="archiving.html">13. Data Compression and Archiving</a><ul>
<li class="toctree-l2"><a class="reference internal" href="zlib.html">13.1. <code class="docutils literal"><span class="pre">zlib</span></code> — Compression compatible with <strong class="program">gzip</strong></a></li>
<li class="toctree-l2"><a class="reference internal" href="gzip.html">13.2. <code class="docutils literal"><span class="pre">gzip</span></code> — Support for <strong class="program">gzip</strong> files</a></li>
<li class="toctree-l2"><a class="reference internal" href="bz2.html">13.3. <code class="docutils literal"><span class="pre">bz2</span></code> — Support for <strong class="program">bzip2</strong> compression</a></li>
<li class="toctree-l2"><a class="reference internal" href="lzma.html">13.4. <code class="docutils literal"><span class="pre">lzma</span></code> — Compression using the LZMA algorithm</a></li>
<li class="toctree-l2"><a class="reference internal" href="zipfile.html">13.5. <code class="docutils literal"><span class="pre">zipfile</span></code> — Work with ZIP archives</a></li>
<li class="toctree-l2"><a class="reference internal" href="tarfile.html">13.6. <code class="docutils literal"><span class="pre">tarfile</span></code> — Read and write tar archive files</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="fileformats.html">14. File Formats</a><ul>
<li class="toctree-l2"><a class="reference internal" href="csv.html">14.1. <code class="docutils literal"><span class="pre">csv</span></code> — CSV File Reading and Writing</a></li>
<li class="toctree-l2"><a class="reference internal" href="configparser.html">14.2. <code class="docutils literal"><span class="pre">configparser</span></code> — Configuration file parser</a></li>
<li class="toctree-l2"><a class="reference internal" href="netrc.html">14.3. <code class="docutils literal"><span class="pre">netrc</span></code> — netrc file processing</a></li>
<li class="toctree-l2"><a class="reference internal" href="xdrlib.html">14.4. <code class="docutils literal"><span class="pre">xdrlib</span></code> — Encode and decode XDR data</a></li>
<li class="toctree-l2"><a class="reference internal" href="plistlib.html">14.5. <code class="docutils literal"><span class="pre">plistlib</span></code> — Generate and parse Mac OS X <code class="docutils literal"><span class="pre">.plist</span></code> files</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="crypto.html">15. Cryptographic Services</a><ul>
<li class="toctree-l2"><a class="reference internal" href="hashlib.html">15.1. <code class="docutils literal"><span class="pre">hashlib</span></code> — Secure hashes and message digests</a></li>
<li class="toctree-l2"><a class="reference internal" href="hmac.html">15.2. <code class="docutils literal"><span class="pre">hmac</span></code> — Keyed-Hashing for Message Authentication</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="allos.html">16. Generic Operating System Services</a><ul>
<li class="toctree-l2"><a class="reference internal" href="os.html">16.1. <code class="docutils literal"><span class="pre">os</span></code> — Miscellaneous operating system interfaces</a></li>
<li class="toctree-l2"><a class="reference internal" href="io.html">16.2. <code class="docutils literal"><span class="pre">io</span></code> — Core tools for working with streams</a></li>
<li class="toctree-l2"><a class="reference internal" href="time.html">16.3. <code class="docutils literal"><span class="pre">time</span></code> — Time access and conversions</a></li>
<li class="toctree-l2"><a class="reference internal" href="argparse.html">16.4. <code class="docutils literal"><span class="pre">argparse</span></code> — Parser for command-line options, arguments and sub-commands</a></li>
<li class="toctree-l2"><a class="reference internal" href="getopt.html">16.5. <code class="docutils literal"><span class="pre">getopt</span></code> — C-style parser for command line options</a></li>
<li class="toctree-l2"><a class="reference internal" href="logging.html">16.6. <code class="docutils literal"><span class="pre">logging</span></code> — Logging facility for Python</a></li>
<li class="toctree-l2"><a class="reference internal" href="logging.config.html">16.7. <code class="docutils literal"><span class="pre">logging.config</span></code> — Logging configuration</a></li>
<li class="toctree-l2"><a class="reference internal" href="logging.handlers.html">16.8. <code class="docutils literal"><span class="pre">logging.handlers</span></code> — Logging handlers</a></li>
<li class="toctree-l2"><a class="reference internal" href="getpass.html">16.9. <code class="docutils literal"><span class="pre">getpass</span></code> — Portable password input</a></li>
<li class="toctree-l2"><a class="reference internal" href="curses.html">16.10. <code class="docutils literal"><span class="pre">curses</span></code> — Terminal handling for character-cell displays</a></li>
<li class="toctree-l2"><a class="reference internal" href="curses.html#module-curses.textpad">16.11. <code class="docutils literal"><span class="pre">curses.textpad</span></code> — Text input widget for curses programs</a></li>
<li class="toctree-l2"><a class="reference internal" href="curses.ascii.html">16.12. <code class="docutils literal"><span class="pre">curses.ascii</span></code> — Utilities for ASCII characters</a></li>
<li class="toctree-l2"><a class="reference internal" href="curses.panel.html">16.13. <code class="docutils literal"><span class="pre">curses.panel</span></code> — A panel stack extension for curses</a></li>
<li class="toctree-l2"><a class="reference internal" href="platform.html">16.14. <code class="docutils literal"><span class="pre">platform</span></code> —  Access to underlying platform’s identifying data</a></li>
<li class="toctree-l2"><a class="reference internal" href="errno.html">16.15. <code class="docutils literal"><span class="pre">errno</span></code> — Standard errno system symbols</a></li>
<li class="toctree-l2"><a class="reference internal" href="ctypes.html">16.16. <code class="docutils literal"><span class="pre">ctypes</span></code> — A foreign function library for Python</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="concurrency.html">17. Concurrent Execution</a><ul>
<li class="toctree-l2"><a class="reference internal" href="threading.html">17.1. <code class="docutils literal"><span class="pre">threading</span></code> — Thread-based parallelism</a></li>
<li class="toctree-l2"><a class="reference internal" href="multiprocessing.html">17.2. <code class="docutils literal"><span class="pre">multiprocessing</span></code> — Process-based parallelism</a></li>
<li class="toctree-l2"><a class="reference internal" href="concurrent.html">17.3. The <code class="docutils literal"><span class="pre">concurrent</span></code> package</a></li>
<li class="toctree-l2"><a class="reference internal" href="concurrent.futures.html">17.4. <code class="docutils literal"><span class="pre">concurrent.futures</span></code> — Launching parallel tasks</a></li>
<li class="toctree-l2"><a class="reference internal" href="subprocess.html">17.5. <code class="docutils literal"><span class="pre">subprocess</span></code> — Subprocess management</a></li>
<li class="toctree-l2"><a class="reference internal" href="sched.html">17.6. <code class="docutils literal"><span class="pre">sched</span></code> — Event scheduler</a></li>
<li class="toctree-l2"><a class="reference internal" href="queue.html">17.7. <code class="docutils literal"><span class="pre">queue</span></code> — A synchronized queue class</a></li>
<li class="toctree-l2"><a class="reference internal" href="dummy_threading.html">17.8. <code class="docutils literal"><span class="pre">dummy_threading</span></code> — Drop-in replacement for the <code class="docutils literal"><span class="pre">threading</span></code> module</a></li>
<li class="toctree-l2"><a class="reference internal" href="_thread.html">17.9. <code class="docutils literal"><span class="pre">_thread</span></code> — Low-level threading API</a></li>
<li class="toctree-l2"><a class="reference internal" href="_dummy_thread.html">17.10. <code class="docutils literal"><span class="pre">_dummy_thread</span></code> — Drop-in replacement for the <code class="docutils literal"><span class="pre">_thread</span></code> module</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="ipc.html">18. Interprocess Communication and Networking</a><ul>
<li class="toctree-l2"><a class="reference internal" href="socket.html">18.1. <code class="docutils literal"><span class="pre">socket</span></code> — Low-level networking interface</a></li>
<li class="toctree-l2"><a class="reference internal" href="ssl.html">18.2. <code class="docutils literal"><span class="pre">ssl</span></code> — TLS/SSL wrapper for socket objects</a></li>
<li class="toctree-l2"><a class="reference internal" href="select.html">18.3. <code class="docutils literal"><span class="pre">select</span></code> — Waiting for I/O completion</a></li>
<li class="toctree-l2"><a class="reference internal" href="selectors.html">18.4. <code class="docutils literal"><span class="pre">selectors</span></code> – High-level I/O multiplexing</a></li>
<li class="toctree-l2"><a class="reference internal" href="asyncio.html">18.5. <code class="docutils literal"><span class="pre">asyncio</span></code> – Asynchronous I/O, event loop, coroutines and tasks</a></li>
<li class="toctree-l2"><a class="reference internal" href="asyncore.html">18.6. <code class="docutils literal"><span class="pre">asyncore</span></code> — Asynchronous socket handler</a></li>
<li class="toctree-l2"><a class="reference internal" href="asynchat.html">18.7. <code class="docutils literal"><span class="pre">asynchat</span></code> — Asynchronous socket command/response handler</a></li>
<li class="toctree-l2"><a class="reference internal" href="signal.html">18.8. <code class="docutils literal"><span class="pre">signal</span></code> — Set handlers for asynchronous events</a></li>
<li class="toctree-l2"><a class="reference internal" href="mmap.html">18.9. <code class="docutils literal"><span class="pre">mmap</span></code> — Memory-mapped file support</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="netdata.html">19. Internet Data Handling</a><ul>
<li class="toctree-l2"><a class="reference internal" href="email.html">19.1. <code class="docutils literal"><span class="pre">email</span></code> — An email and MIME handling package</a></li>
<li class="toctree-l2"><a class="reference internal" href="json.html">19.2. <code class="docutils literal"><span class="pre">json</span></code> — JSON encoder and decoder</a></li>
<li class="toctree-l2"><a class="reference internal" href="mailcap.html">19.3. <code class="docutils literal"><span class="pre">mailcap</span></code> — Mailcap file handling</a></li>
<li class="toctree-l2"><a class="reference internal" href="mailbox.html">19.4. <code class="docutils literal"><span class="pre">mailbox</span></code> — Manipulate mailboxes in various formats</a></li>
<li class="toctree-l2"><a class="reference internal" href="mimetypes.html">19.5. <code class="docutils literal"><span class="pre">mimetypes</span></code> — Map filenames to MIME types</a></li>
<li class="toctree-l2"><a class="reference internal" href="base64.html">19.6. <code class="docutils literal"><span class="pre">base64</span></code> — Base16, Base32, Base64, Base85 Data Encodings</a></li>
<li class="toctree-l2"><a class="reference internal" href="binhex.html">19.7. <code class="docutils literal"><span class="pre">binhex</span></code> — Encode and decode binhex4 files</a></li>
<li class="toctree-l2"><a class="reference internal" href="binascii.html">19.8. <code class="docutils literal"><span class="pre">binascii</span></code> — Convert between binary and ASCII</a></li>
<li class="toctree-l2"><a class="reference internal" href="quopri.html">19.9. <code class="docutils literal"><span class="pre">quopri</span></code> — Encode and decode MIME quoted-printable data</a></li>
<li class="toctree-l2"><a class="reference internal" href="uu.html">19.10. <code class="docutils literal"><span class="pre">uu</span></code> — Encode and decode uuencode files</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="markup.html">20. Structured Markup Processing Tools</a><ul>
<li class="toctree-l2"><a class="reference internal" href="html.html">20.1. <code class="docutils literal"><span class="pre">html</span></code> — HyperText Markup Language support</a></li>
<li class="toctree-l2"><a class="reference internal" href="html.parser.html">20.2. <code class="docutils literal"><span class="pre">html.parser</span></code> — Simple HTML and XHTML parser</a></li>
<li class="toctree-l2"><a class="reference internal" href="html.entities.html">20.3. <code class="docutils literal"><span class="pre">html.entities</span></code> — Definitions of HTML general entities</a></li>
<li class="toctree-l2"><a class="reference internal" href="xml.html">20.4. XML Processing Modules</a></li>
<li class="toctree-l2"><a class="reference internal" href="xml.etree.elementtree.html">20.5. <code class="docutils literal"><span class="pre">xml.etree.ElementTree</span></code> — The ElementTree XML API</a></li>
<li class="toctree-l2"><a class="reference internal" href="xml.dom.html">20.6. <code class="docutils literal"><span class="pre">xml.dom</span></code> — The Document Object Model API</a></li>
<li class="toctree-l2"><a class="reference internal" href="xml.dom.minidom.html">20.7. <code class="docutils literal"><span class="pre">xml.dom.minidom</span></code> — Minimal DOM implementation</a></li>
<li class="toctree-l2"><a class="reference internal" href="xml.dom.pulldom.html">20.8. <code class="docutils literal"><span class="pre">xml.dom.pulldom</span></code> — Support for building partial DOM trees</a></li>
<li class="toctree-l2"><a class="reference internal" href="xml.sax.html">20.9. <code class="docutils literal"><span class="pre">xml.sax</span></code> — Support for SAX2 parsers</a></li>
<li class="toctree-l2"><a class="reference internal" href="xml.sax.handler.html">20.10. <code class="docutils literal"><span class="pre">xml.sax.handler</span></code> — Base classes for SAX handlers</a></li>
<li class="toctree-l2"><a class="reference internal" href="xml.sax.utils.html">20.11. <code class="docutils literal"><span class="pre">xml.sax.saxutils</span></code> — SAX Utilities</a></li>
<li class="toctree-l2"><a class="reference internal" href="xml.sax.reader.html">20.12. <code class="docutils literal"><span class="pre">xml.sax.xmlreader</span></code> — Interface for XML parsers</a></li>
<li class="toctree-l2"><a class="reference internal" href="pyexpat.html">20.13. <code class="docutils literal"><span class="pre">xml.parsers.expat</span></code> — Fast XML parsing using Expat</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="internet.html">21. Internet Protocols and Support</a><ul>
<li class="toctree-l2"><a class="reference internal" href="webbrowser.html">21.1. <code class="docutils literal"><span class="pre">webbrowser</span></code> — Convenient Web-browser controller</a></li>
<li class="toctree-l2"><a class="reference internal" href="cgi.html">21.2. <code class="docutils literal"><span class="pre">cgi</span></code> — Common Gateway Interface support</a></li>
<li class="toctree-l2"><a class="reference internal" href="cgitb.html">21.3. <code class="docutils literal"><span class="pre">cgitb</span></code> — Traceback manager for CGI scripts</a></li>
<li class="toctree-l2"><a class="reference internal" href="wsgiref.html">21.4. <code class="docutils literal"><span class="pre">wsgiref</span></code> — WSGI Utilities and Reference Implementation</a></li>
<li class="toctree-l2"><a class="reference internal" href="urllib.html">21.5. <code class="docutils literal"><span class="pre">urllib</span></code> — URL handling modules</a></li>
<li class="toctree-l2"><a class="reference internal" href="urllib.request.html">21.6. <code class="docutils literal"><span class="pre">urllib.request</span></code> — Extensible library for opening URLs</a></li>
<li class="toctree-l2"><a class="reference internal" href="urllib.request.html#module-urllib.response">21.7. <code class="docutils literal"><span class="pre">urllib.response</span></code> — Response classes used by urllib</a></li>
<li class="toctree-l2"><a class="reference internal" href="urllib.parse.html">21.8. <code class="docutils literal"><span class="pre">urllib.parse</span></code> — Parse URLs into components</a></li>
<li class="toctree-l2"><a class="reference internal" href="urllib.error.html">21.9. <code class="docutils literal"><span class="pre">urllib.error</span></code> — Exception classes raised by urllib.request</a></li>
<li class="toctree-l2"><a class="reference internal" href="urllib.robotparser.html">21.10. <code class="docutils literal"><span class="pre">urllib.robotparser</span></code> —  Parser for robots.txt</a></li>
<li class="toctree-l2"><a class="reference internal" href="http.html">21.11. <code class="docutils literal"><span class="pre">http</span></code> — HTTP modules</a></li>
<li class="toctree-l2"><a class="reference internal" href="http.client.html">21.12. <code class="docutils literal"><span class="pre">http.client</span></code> — HTTP protocol client</a></li>
<li class="toctree-l2"><a class="reference internal" href="ftplib.html">21.13. <code class="docutils literal"><span class="pre">ftplib</span></code> — FTP protocol client</a></li>
<li class="toctree-l2"><a class="reference internal" href="poplib.html">21.14. <code class="docutils literal"><span class="pre">poplib</span></code> — POP3 protocol client</a></li>
<li class="toctree-l2"><a class="reference internal" href="imaplib.html">21.15. <code class="docutils literal"><span class="pre">imaplib</span></code> — IMAP4 protocol client</a></li>
<li class="toctree-l2"><a class="reference internal" href="nntplib.html">21.16. <code class="docutils literal"><span class="pre">nntplib</span></code> — NNTP protocol client</a></li>
<li class="toctree-l2"><a class="reference internal" href="smtplib.html">21.17. <code class="docutils literal"><span class="pre">smtplib</span></code> — SMTP protocol client</a></li>
<li class="toctree-l2"><a class="reference internal" href="smtpd.html">21.18. <code class="docutils literal"><span class="pre">smtpd</span></code> — SMTP Server</a></li>
<li class="toctree-l2"><a class="reference internal" href="telnetlib.html">21.19. <code class="docutils literal"><span class="pre">telnetlib</span></code> — Telnet client</a></li>
<li class="toctree-l2"><a class="reference internal" href="uuid.html">21.20. <code class="docutils literal"><span class="pre">uuid</span></code> — UUID objects according to RFC 4122</a></li>
<li class="toctree-l2"><a class="reference internal" href="socketserver.html">21.21. <code class="docutils literal"><span class="pre">socketserver</span></code> — A framework for network servers</a></li>
<li class="toctree-l2"><a class="reference internal" href="http.server.html">21.22. <code class="docutils literal"><span class="pre">http.server</span></code> — HTTP servers</a></li>
<li class="toctree-l2"><a class="reference internal" href="http.cookies.html">21.23. <code class="docutils literal"><span class="pre">http.cookies</span></code> — HTTP state management</a></li>
<li class="toctree-l2"><a class="reference internal" href="http.cookiejar.html">21.24. <code class="docutils literal"><span class="pre">http.cookiejar</span></code> — Cookie handling for HTTP clients</a></li>
<li class="toctree-l2"><a class="reference internal" href="xmlrpc.html">21.25. <code class="docutils literal"><span class="pre">xmlrpc</span></code> — XMLRPC server and client modules</a></li>
<li class="toctree-l2"><a class="reference internal" href="xmlrpc.client.html">21.26. <code class="docutils literal"><span class="pre">xmlrpc.client</span></code> — XML-RPC client access</a></li>
<li class="toctree-l2"><a class="reference internal" href="xmlrpc.server.html">21.27. <code class="docutils literal"><span class="pre">xmlrpc.server</span></code> — Basic XML-RPC servers</a></li>
<li class="toctree-l2"><a class="reference internal" href="ipaddress.html">21.28. <code class="docutils literal"><span class="pre">ipaddress</span></code> — IPv4/IPv6 manipulation library</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="mm.html">22. Multimedia Services</a><ul>
<li class="toctree-l2"><a class="reference internal" href="audioop.html">22.1. <code class="docutils literal"><span class="pre">audioop</span></code> — Manipulate raw audio data</a></li>
<li class="toctree-l2"><a class="reference internal" href="aifc.html">22.2. <code class="docutils literal"><span class="pre">aifc</span></code> — Read and write AIFF and AIFC files</a></li>
<li class="toctree-l2"><a class="reference internal" href="sunau.html">22.3. <code class="docutils literal"><span class="pre">sunau</span></code> — Read and write Sun AU files</a></li>
<li class="toctree-l2"><a class="reference internal" href="wave.html">22.4. <code class="docutils literal"><span class="pre">wave</span></code> — Read and write WAV files</a></li>
<li class="toctree-l2"><a class="reference internal" href="chunk.html">22.5. <code class="docutils literal"><span class="pre">chunk</span></code> — Read IFF chunked data</a></li>
<li class="toctree-l2"><a class="reference internal" href="colorsys.html">22.6. <code class="docutils literal"><span class="pre">colorsys</span></code> — Conversions between color systems</a></li>
<li class="toctree-l2"><a class="reference internal" href="imghdr.html">22.7. <code class="docutils literal"><span class="pre">imghdr</span></code> — Determine the type of an image</a></li>
<li class="toctree-l2"><a class="reference internal" href="sndhdr.html">22.8. <code class="docutils literal"><span class="pre">sndhdr</span></code> — Determine type of sound file</a></li>
<li class="toctree-l2"><a class="reference internal" href="ossaudiodev.html">22.9. <code class="docutils literal"><span class="pre">ossaudiodev</span></code> — Access to OSS-compatible audio devices</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="i18n.html">23. Internationalization</a><ul>
<li class="toctree-l2"><a class="reference internal" href="gettext.html">23.1. <code class="docutils literal"><span class="pre">gettext</span></code> — Multilingual internationalization services</a></li>
<li class="toctree-l2"><a class="reference internal" href="locale.html">23.2. <code class="docutils literal"><span class="pre">locale</span></code> — Internationalization services</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="frameworks.html">24. Program Frameworks</a><ul>
<li class="toctree-l2"><a class="reference internal" href="turtle.html">24.1. <code class="docutils literal"><span class="pre">turtle</span></code> — Turtle graphics</a></li>
<li class="toctree-l2"><a class="reference internal" href="cmd.html">24.2. <code class="docutils literal"><span class="pre">cmd</span></code> — Support for line-oriented command interpreters</a></li>
<li class="toctree-l2"><a class="reference internal" href="shlex.html">24.3. <code class="docutils literal"><span class="pre">shlex</span></code> — Simple lexical analysis</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="tk.html">25. Graphical User Interfaces with Tk</a><ul>
<li class="toctree-l2"><a class="reference internal" href="tkinter.html">25.1. <code class="docutils literal"><span class="pre">tkinter</span></code> — Python interface to Tcl/Tk</a></li>
<li class="toctree-l2"><a class="reference internal" href="tkinter.ttk.html">25.2. <code class="docutils literal"><span class="pre">tkinter.ttk</span></code> — Tk themed widgets</a></li>
<li class="toctree-l2"><a class="reference internal" href="tkinter.tix.html">25.3. <code class="docutils literal"><span class="pre">tkinter.tix</span></code> — Extension widgets for Tk</a></li>
<li class="toctree-l2"><a class="reference internal" href="tkinter.scrolledtext.html">25.4. <code class="docutils literal"><span class="pre">tkinter.scrolledtext</span></code> — Scrolled Text Widget</a></li>
<li class="toctree-l2"><a class="reference internal" href="idle.html">25.5. IDLE</a></li>
<li class="toctree-l2"><a class="reference internal" href="othergui.html">25.6. Other Graphical User Interface Packages</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="development.html">26. Development Tools</a><ul>
<li class="toctree-l2"><a class="reference internal" href="typing.html">26.1. <code class="docutils literal"><span class="pre">typing</span></code> — Support for type hints</a></li>
<li class="toctree-l2"><a class="reference internal" href="pydoc.html">26.2. <code class="docutils literal"><span class="pre">pydoc</span></code> — Documentation generator and online help system</a></li>
<li class="toctree-l2"><a class="reference internal" href="doctest.html">26.3. <code class="docutils literal"><span class="pre">doctest</span></code> — Test interactive Python examples</a></li>
<li class="toctree-l2"><a class="reference internal" href="unittest.html">26.4. <code class="docutils literal"><span class="pre">unittest</span></code> — Unit testing framework</a></li>
<li class="toctree-l2"><a class="reference internal" href="unittest.mock.html">26.5. <code class="docutils literal"><span class="pre">unittest.mock</span></code> — mock object library</a></li>
<li class="toctree-l2"><a class="reference internal" href="unittest.mock-examples.html">26.6. <code class="docutils literal"><span class="pre">unittest.mock</span></code> — getting started</a></li>
<li class="toctree-l2"><a class="reference internal" href="2to3.html">26.7. 2to3 - Automated Python 2 to 3 code translation</a></li>
<li class="toctree-l2"><a class="reference internal" href="test.html">26.8. <code class="docutils literal"><span class="pre">test</span></code> — Regression tests package for Python</a></li>
<li class="toctree-l2"><a class="reference internal" href="test.html#module-test.support">26.9. <code class="docutils literal"><span class="pre">test.support</span></code> — Utilities for the Python test suite</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="debug.html">27. Debugging and Profiling</a><ul>
<li class="toctree-l2"><a class="reference internal" href="bdb.html">27.1. <code class="docutils literal"><span class="pre">bdb</span></code> — Debugger framework</a></li>
<li class="toctree-l2"><a class="reference internal" href="faulthandler.html">27.2. <code class="docutils literal"><span class="pre">faulthandler</span></code> — Dump the Python traceback</a></li>
<li class="toctree-l2"><a class="reference internal" href="pdb.html">27.3. <code class="docutils literal"><span class="pre">pdb</span></code> — The Python Debugger</a></li>
<li class="toctree-l2"><a class="reference internal" href="profile.html">27.4. The Python Profilers</a></li>
<li class="toctree-l2"><a class="reference internal" href="timeit.html">27.5. <code class="docutils literal"><span class="pre">timeit</span></code> — Measure execution time of small code snippets</a></li>
<li class="toctree-l2"><a class="reference internal" href="trace.html">27.6. <code class="docutils literal"><span class="pre">trace</span></code> — Trace or track Python statement execution</a></li>
<li class="toctree-l2"><a class="reference internal" href="tracemalloc.html">27.7. <code class="docutils literal"><span class="pre">tracemalloc</span></code> — Trace memory allocations</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="distribution.html">28. Software Packaging and Distribution</a><ul>
<li class="toctree-l2"><a class="reference internal" href="distutils.html">28.1. <code class="docutils literal"><span class="pre">distutils</span></code> — Building and installing Python modules</a></li>
<li class="toctree-l2"><a class="reference internal" href="ensurepip.html">28.2. <code class="docutils literal"><span class="pre">ensurepip</span></code> — Bootstrapping the <code class="docutils literal"><span class="pre">pip</span></code> installer</a></li>
<li class="toctree-l2"><a class="reference internal" href="venv.html">28.3. <code class="docutils literal"><span class="pre">venv</span></code> — Creation of virtual environments</a></li>
<li class="toctree-l2"><a class="reference internal" href="zipapp.html">28.4. <code class="docutils literal"><span class="pre">zipapp</span></code> — Manage executable python zip archives</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="python.html">29. Python Runtime Services</a><ul>
<li class="toctree-l2"><a class="reference internal" href="sys.html">29.1. <code class="docutils literal"><span class="pre">sys</span></code> — System-specific parameters and functions</a></li>
<li class="toctree-l2"><a class="reference internal" href="sysconfig.html">29.2. <code class="docutils literal"><span class="pre">sysconfig</span></code> — Provide access to Python’s configuration information</a></li>
<li class="toctree-l2"><a class="reference internal" href="builtins.html">29.3. <code class="docutils literal"><span class="pre">builtins</span></code> — Built-in objects</a></li>
<li class="toctree-l2"><a class="reference internal" href="__main__.html">29.4. <code class="docutils literal"><span class="pre">__main__</span></code> — Top-level script environment</a></li>
<li class="toctree-l2"><a class="reference internal" href="warnings.html">29.5. <code class="docutils literal"><span class="pre">warnings</span></code> — Warning control</a></li>
<li class="toctree-l2"><a class="reference internal" href="contextlib.html">29.6. <code class="docutils literal"><span class="pre">contextlib</span></code> — Utilities for <code class="docutils literal"><span class="pre">with</span></code>-statement contexts</a></li>
<li class="toctree-l2"><a class="reference internal" href="abc.html">29.7. <code class="docutils literal"><span class="pre">abc</span></code> — Abstract Base Classes</a></li>
<li class="toctree-l2"><a class="reference internal" href="atexit.html">29.8. <code class="docutils literal"><span class="pre">atexit</span></code> — Exit handlers</a></li>
<li class="toctree-l2"><a class="reference internal" href="traceback.html">29.9. <code class="docutils literal"><span class="pre">traceback</span></code> — Print or retrieve a stack traceback</a></li>
<li class="toctree-l2"><a class="reference internal" href="__future__.html">29.10. <code class="docutils literal"><span class="pre">__future__</span></code> — Future statement definitions</a></li>
<li class="toctree-l2"><a class="reference internal" href="gc.html">29.11. <code class="docutils literal"><span class="pre">gc</span></code> — Garbage Collector interface</a></li>
<li class="toctree-l2"><a class="reference internal" href="inspect.html">29.12. <code class="docutils literal"><span class="pre">inspect</span></code> — Inspect live objects</a></li>
<li class="toctree-l2"><a class="reference internal" href="site.html">29.13. <code class="docutils literal"><span class="pre">site</span></code> — Site-specific configuration hook</a></li>
<li class="toctree-l2"><a class="reference internal" href="fpectl.html">29.14. <code class="docutils literal"><span class="pre">fpectl</span></code> — Floating point exception control</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="custominterp.html">30. Custom Python Interpreters</a><ul>
<li class="toctree-l2"><a class="reference internal" href="code.html">30.1. <code class="docutils literal"><span class="pre">code</span></code> — Interpreter base classes</a></li>
<li class="toctree-l2"><a class="reference internal" href="codeop.html">30.2. <code class="docutils literal"><span class="pre">codeop</span></code> — Compile Python code</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="modules.html">31. Importing Modules</a><ul>
<li class="toctree-l2"><a class="reference internal" href="zipimport.html">31.1. <code class="docutils literal"><span class="pre">zipimport</span></code> — Import modules from Zip archives</a></li>
<li class="toctree-l2"><a class="reference internal" href="pkgutil.html">31.2. <code class="docutils literal"><span class="pre">pkgutil</span></code> — Package extension utility</a></li>
<li class="toctree-l2"><a class="reference internal" href="modulefinder.html">31.3. <code class="docutils literal"><span class="pre">modulefinder</span></code> — Find modules used by a script</a></li>
<li class="toctree-l2"><a class="reference internal" href="runpy.html">31.4. <code class="docutils literal"><span class="pre">runpy</span></code> — Locating and executing Python modules</a></li>
<li class="toctree-l2"><a class="reference internal" href="importlib.html">31.5. <code class="docutils literal"><span class="pre">importlib</span></code> – The implementation of <code class="docutils literal"><span class="pre">import</span></code></a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="language.html">32. Python Language Services</a><ul>
<li class="toctree-l2"><a class="reference internal" href="parser.html">32.1. <code class="docutils literal"><span class="pre">parser</span></code> — Access Python parse trees</a></li>
<li class="toctree-l2"><a class="reference internal" href="ast.html">32.2. <code class="docutils literal"><span class="pre">ast</span></code> — Abstract Syntax Trees</a></li>
<li class="toctree-l2"><a class="reference internal" href="symtable.html">32.3. <code class="docutils literal"><span class="pre">symtable</span></code> — Access to the compiler’s symbol tables</a></li>
<li class="toctree-l2"><a class="reference internal" href="symbol.html">32.4. <code class="docutils literal"><span class="pre">symbol</span></code> — Constants used with Python parse trees</a></li>
<li class="toctree-l2"><a class="reference internal" href="token.html">32.5. <code class="docutils literal"><span class="pre">token</span></code> — Constants used with Python parse trees</a></li>
<li class="toctree-l2"><a class="reference internal" href="keyword.html">32.6. <code class="docutils literal"><span class="pre">keyword</span></code> — Testing for Python keywords</a></li>
<li class="toctree-l2"><a class="reference internal" href="tokenize.html">32.7. <code class="docutils literal"><span class="pre">tokenize</span></code> — Tokenizer for Python source</a></li>
<li class="toctree-l2"><a class="reference internal" href="tabnanny.html">32.8. <code class="docutils literal"><span class="pre">tabnanny</span></code> — Detection of ambiguous indentation</a></li>
<li class="toctree-l2"><a class="reference internal" href="pyclbr.html">32.9. <code class="docutils literal"><span class="pre">pyclbr</span></code> — Python class browser support</a></li>
<li class="toctree-l2"><a class="reference internal" href="py_compile.html">32.10. <code class="docutils literal"><span class="pre">py_compile</span></code> — Compile Python source files</a></li>
<li class="toctree-l2"><a class="reference internal" href="compileall.html">32.11. <code class="docutils literal"><span class="pre">compileall</span></code> — Byte-compile Python libraries</a></li>
<li class="toctree-l2"><a class="reference internal" href="dis.html">32.12. <code class="docutils literal"><span class="pre">dis</span></code> — Disassembler for Python bytecode</a></li>
<li class="toctree-l2"><a class="reference internal" href="pickletools.html">32.13. <code class="docutils literal"><span class="pre">pickletools</span></code> — Tools for pickle developers</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="misc.html">33. Miscellaneous Services</a><ul>
<li class="toctree-l2"><a class="reference internal" href="formatter.html">33.1. <code class="docutils literal"><span class="pre">formatter</span></code> — Generic output formatting</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="windows.html">34. MS Windows Specific Services</a><ul>
<li class="toctree-l2"><a class="reference internal" href="msilib.html">34.1. <code class="docutils literal"><span class="pre">msilib</span></code> — Read and write Microsoft Installer files</a></li>
<li class="toctree-l2"><a class="reference internal" href="msvcrt.html">34.2. <code class="docutils literal"><span class="pre">msvcrt</span></code> – Useful routines from the MS VC++ runtime</a></li>
<li class="toctree-l2"><a class="reference internal" href="winreg.html">34.3. <code class="docutils literal"><span class="pre">winreg</span></code> – Windows registry access</a></li>
<li class="toctree-l2"><a class="reference internal" href="winsound.html">34.4. <code class="docutils literal"><span class="pre">winsound</span></code> — Sound-playing interface for Windows</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="unix.html">35. Unix Specific Services</a><ul>
<li class="toctree-l2"><a class="reference internal" href="posix.html">35.1. <code class="docutils literal"><span class="pre">posix</span></code> — The most common POSIX system calls</a></li>
<li class="toctree-l2"><a class="reference internal" href="pwd.html">35.2. <code class="docutils literal"><span class="pre">pwd</span></code> — The password database</a></li>
<li class="toctree-l2"><a class="reference internal" href="spwd.html">35.3. <code class="docutils literal"><span class="pre">spwd</span></code> — The shadow password database</a></li>
<li class="toctree-l2"><a class="reference internal" href="grp.html">35.4. <code class="docutils literal"><span class="pre">grp</span></code> — The group database</a></li>
<li class="toctree-l2"><a class="reference internal" href="crypt.html">35.5. <code class="docutils literal"><span class="pre">crypt</span></code> — Function to check Unix passwords</a></li>
<li class="toctree-l2"><a class="reference internal" href="termios.html">35.6. <code class="docutils literal"><span class="pre">termios</span></code> — POSIX style tty control</a></li>
<li class="toctree-l2"><a class="reference internal" href="tty.html">35.7. <code class="docutils literal"><span class="pre">tty</span></code> — Terminal control functions</a></li>
<li class="toctree-l2"><a class="reference internal" href="pty.html">35.8. <code class="docutils literal"><span class="pre">pty</span></code> — Pseudo-terminal utilities</a></li>
<li class="toctree-l2"><a class="reference internal" href="fcntl.html">35.9. <code class="docutils literal"><span class="pre">fcntl</span></code> — The <code class="docutils literal"><span class="pre">fcntl</span></code> and <code class="docutils literal"><span class="pre">ioctl</span></code> system calls</a></li>
<li class="toctree-l2"><a class="reference internal" href="pipes.html">35.10. <code class="docutils literal"><span class="pre">pipes</span></code> — Interface to shell pipelines</a></li>
<li class="toctree-l2"><a class="reference internal" href="resource.html">35.11. <code class="docutils literal"><span class="pre">resource</span></code> — Resource usage information</a></li>
<li class="toctree-l2"><a class="reference internal" href="nis.html">35.12. <code class="docutils literal"><span class="pre">nis</span></code> — Interface to Sun’s NIS (Yellow Pages)</a></li>
<li class="toctree-l2"><a class="reference internal" href="syslog.html">35.13. <code class="docutils literal"><span class="pre">syslog</span></code> — Unix syslog library routines</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="superseded.html">36. Superseded Modules</a><ul>
<li class="toctree-l2"><a class="reference internal" href="optparse.html">36.1. <code class="docutils literal"><span class="pre">optparse</span></code> — Parser for command line options</a></li>
<li class="toctree-l2"><a class="reference internal" href="imp.html">36.2. <code class="docutils literal"><span class="pre">imp</span></code> — Access the <code class="docutils literal"><span class="pre">import</span></code> internals</a></li>
</ul>
</li>
<li class="toctree-l1"><a class="reference internal" href="undoc.html">37. Undocumented Modules</a><ul>
<li class="toctree-l2"><a class="reference internal" href="undoc.html#platform-specific-modules">37.1. Platform specific modules</a></li>
</ul>
</li>
</ul>
</div>
