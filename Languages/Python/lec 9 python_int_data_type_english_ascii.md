# PYTHON DATA TYPES — `int` DATA TYPE AND NUMBER SYSTEMS

> Clean English translation of the supplied lecture transcript.
> The original teaching order, examples, warnings, and homework are retained.
> Where the source speech/transcription contains an inconsistent number or unclear word, it is marked as **[as spoken]** or **[unclear in source]** rather than silently corrected.

-------------------------------------------------------------------------------
## 00:00 — INTRODUCTION
-------------------------------------------------------------------------------

**00:00**  [Music]

**00:09**  Good morning, Namaste, Assalam-o-Alaikum, friends. I am here with a new Python lecture. Today we are going to start data types.

**00:16**  In the previous lecture, I told you that we have 14 types of data types.

**00:23**  Those data types are divided into six categories. You have already seen that overview.

**00:30**  Today I am going to start with the `int` data type. We will begin here and then continue in sequence.

**00:36**  First, we will study the numeric data types, and then we will study the remaining data types one by one.

**00:42**  In today’s complete lecture, I will explain all the important points related to the integer (`int`) type.

**00:47**  After this lecture, you should be able to answer questions related to the integer type.

**00:52**  Whether the question appears in an interview, a competitive exam, or somewhere else, you should be able to answer it easily. So let us begin.

-------------------------------------------------------------------------------
## 01:00 — IMPORTANT BUILT-IN FEATURES: `type()`, `id()`, `print()`
-------------------------------------------------------------------------------

**01:00**  Before we start, there are one or two important things that we will use in commands. I have used them before, but I will explain them again.

**01:06**  I want you to know what we are doing when we use them later.

**01:12**  After that, we will come directly to the integer type. These are some built-in features that we have already used many times.

**01:19**  You may not know them clearly if you are learning Python, or programming in general, for the first time.

**01:24**  Every programming language has built-in features. When we use a particular built-in feature, the language understands what operation we want it to perform.

**01:31**  Examples include:

```text
`type()`
`id()`
`print()`
```

**01:38**  These are very common. We will keep using them continuously, so there is no need to worry.

**01:44**  I have already shown you `print()` many times. The point is that these three features will be used regularly throughout Python.

**01:50**  Therefore, we should know that these are built-in Python features and what result each one gives us.

### `type()`

**01:58**  If I want to check the type of something — for example, whether it is an integer, a float, or something else — I use `type()`.

**02:06**  Inside the parentheses, I write the name of the object or variable whose type I want to check.

**02:13**  For example, suppose I write:

```python
a = 100
```

**02:20**  I have stored the value `100` inside `a`. Now suppose I change it to:

```python
a = 100.5
```

**02:27**  Now it becomes a floating-point value. Suppose I do not know its type, or I want to verify whether it is `int`, `float`, or something else.

**02:34**  What will you do? You can print the value and also check its type.

**02:40**  Remember that `print()` is also a built-in feature. We will discuss it more as we continue.

**02:48**  You could write something like:

```python
print(a)
print(type(a))
```

**02:56**  Or you can directly print the result of `type(a)`.

**03:01**  There are several ways to inspect values and their types, and we will learn them.

**03:09**  If `a = 100.5`, the result will show the value `100.5`, and its type will appear as a class.

**03:16**  It will show `float`, because `100.5` is a floating-point number.

**03:23**  In Python, the class shown by `type()` represents the data type.

**03:30**  So when you use `type()`, the output may show something like:

```text
<class 'float'>
```

**03:36**  Python normally shows the class name rather than writing the words “data type”.

### `id()` and memory identity

**03:36**  Next is `id()`. I previously mentioned mutable and immutable objects.

**03:42**  Some students commented that they did not understand “immutable”. We will study that in detail later.

**03:49**  In the earlier lecture, it was only an overview. I had already said that I would explain it later.

**03:56**  Suppose you want to know where a value is stored in memory.

**04:01**  Imagine memory as a large area divided into many spaces or locations.

**04:09**  Suppose the value `100` is stored in one of those memory locations, and that location has an identity number such as `2043`.

**04:16**  That identity number is what we are discussing as the memory ID.

**04:21**  If you want to check the memory identity associated with an object such as the value `100`, Python can give you that information.

**04:27**  You can use `id()` to get a numeric identity value.

**04:34**  That value tells you the identity associated with the object in memory. This is what we are calling the memory ID here.

**04:41**  In simple words, that is the identity of the location/object where the value is being held.

**04:47**  Now, regarding mutability: if something can be changed while keeping the same identity, it is called mutable.

**04:53**  That is, if you change its contents but the identity does not change, then it is mutable.

**04:58**  We will study this topic in more detail later. For now, remember that `id()` lets you inspect an object’s identity.

**05:05**  It helps you see the identity associated with where that data exists in the system.

### `print()`

**05:10**  We have already been using `print()`.

**05:17**  If a value is stored somewhere and you want to see it, you use `print()`.

**05:23**  It lets you display the value stored in a variable.

**05:28**  For example:

```python
a = 100
b = 200
c = a + b
```

**05:35**  If I do not want to calculate the sum manually, I can print `c`.

**05:40**  Python adds `a` and `b` and shows the result.

**05:47**  In general, `print()` is used when you want to see a value, an output, or something stored inside a variable.

**05:53**  In the example above, `c` stores the result of `a + b`.

**05:58**  Python adds the two values and stores the result in `c`.

**06:05**  When I write `print(c)`, Python displays the value of `c`.

**06:10**  These are built-in features that we will use continuously, so I explained them before starting the integer type.

-------------------------------------------------------------------------------
## 06:15 — BASIC IDEA OF THE `int` DATA TYPE
-------------------------------------------------------------------------------

**06:15**  Now let us discuss the `int` data type and some of its basic points.

**06:22**  We use the `int` data type to represent whole numbers or integral values.

**06:28**  In simple language, if a number does not have a fractional/decimal part after a point, it can be represented as an integer.

**06:35**  For example, `22.5` has a value after the decimal point.

**06:41**  A value with no fractional part after the decimal point is a whole number/integral value.

**06:47**  We use the integer type to represent such data.

**06:52**  For example:

```python
a = 100
```

**06:58**  The value `100` has been stored in a variable called `a`.

**07:04**  `a` is the variable/identifier name used to refer to that value.

**07:09**  The instructor uses terms such as identifier, value, and object while explaining; do not let the terminology confuse you.

**07:15**  Study carefully and follow the programming concepts step by step.

**07:21–07:48**  The instructor says the full course will be taught in detail, rather than giving only partial lessons. He encourages students to study with the same level of detail because many other courses finish these topics much more quickly.

-------------------------------------------------------------------------------
## 07:56 — CHECKING VALUE, TYPE, AND ID
-------------------------------------------------------------------------------

**07:56**  We stored `100` in `a`. Earlier, I explained built-in features such as `print()`.

**08:02**  Whatever we place inside `print(...)` can be displayed.

**08:07**  Remember the parentheses. The instructor jokingly reminds students not to forget what was just explained.

**08:14**  If we place `a` inside the parentheses, Python prints the value of `a`.

**08:20**  This was also demonstrated in the previous lab/video.

**08:27**  Because `a` contains `100`, Python displays:

```text
100
```

**08:33**  If you now want to know the data type/class of `a`, you can use `type(a)`.

**08:39**  You may want to know whether it is `int`, `float`, `bool`, or another type.

**08:44**  `type(a)` will show that the value is of integer type.

**08:51**  Python identifies this automatically; this is part of Python’s dynamic nature.

**08:57**  To inspect its identity, use `id(a)`.

**09:03**  The returned number may be different on different runs/systems.

**09:09**  That number represents the object’s identity in memory.

-------------------------------------------------------------------------------
## 09:14 — PYTHON 2 `long` VS PYTHON 3 `int`
-------------------------------------------------------------------------------

**09:14**  The lecture is using Python 3.11 at the time of recording.

**09:22**  In the future, the minor version may be 3.12, 3.13, 3.14, and so on.

**09:28**  The exact minor version is less important than understanding that we are learning Python 3.

**09:36**  So whether you see Python 3.11, 3.13, or another Python 3 version, the lecture is about Python 3 concepts.

**09:49**  Before Python 3, Python 2.x existed.

**09:57**  Python 2 had a separate `long` integer type for very large integer values.

**10:02**  Similar ideas may also be familiar from languages such as C or C++.

**10:08**  If you have not studied those languages, just remember the main idea.

**10:14**  In older systems/languages, a separate type could be needed for larger integer values.

**10:21**  In Python 3, this issue is simplified.

**10:26**  Python 3 does not have a separate explicit `long` type.

**10:33**  Normal Python 3 integers can grow to very large values, subject to available memory.

**10:39**  You do not need to switch to a separate `long` or similar integer class just because the number becomes large.

**10:46**  Python 3 therefore simplifies integer handling.

**10:53**  Among the predefined data types being studied, you can continue to use `int` for very large whole-number values.

**11:01**  You do not need a separate category simply because the integer is large.

-------------------------------------------------------------------------------
## 11:16 — NUMBER SYSTEMS OVERVIEW
-------------------------------------------------------------------------------

**11:16**  The integer type can also represent data written using different number systems.

**11:23**  Many students are non-technical, so the instructor first explains what a number system is.

**11:31**  The number system we normally use in everyday life is called the decimal number system.

**11:38**  For example, if you see `200`, you normally read it as two hundred.

**11:44**  If you see `100`, you normally read it as one hundred.

**11:50**  If you see something like `8314`, you may naturally read it as eight thousand three hundred fourteen.

**11:58–12:08**  But if a base is written with a number, its meaning depends on that number system. The instructor gives an example and corrects himself while speaking.

**12:16**  There are several number systems. The one we normally use is decimal.

**12:22**  Decimal has base 10.

**12:28**  In normal usage, we do not usually need to write the base because decimal is understood by default.

**12:35**  If we use another number system, however, we need some way to indicate which number system is being used.

**12:42**  This is important, and the instructor will show how it is written in Python.

**12:50**  Python integers can be represented using four common number-system forms discussed in this lecture.

**12:56**  These are decimal, binary, octal, and hexadecimal.

**13:01**  Questions about these forms can appear in exams.

**13:06**  The same integer concept can be represented using these different number systems.

**13:12**  However, when you print such an integer normally in Python, the displayed output is decimal by default.

**13:20**  Whether the value was written in binary, hexadecimal, or octal notation, normal `print()` output is shown in decimal form.

**13:33**  The instructor explains this as a human-readable/default representation.

**13:44**  Humans commonly understand ordinary decimal notation such as `200`.

-------------------------------------------------------------------------------
## 13:57 — DECIMAL, BINARY, OCTAL, HEXADECIMAL DIGITS
-------------------------------------------------------------------------------

### Decimal

**13:57**  Numbers such as 1000, 200, 550, and so on are normally written in decimal notation.

**14:03**  Decimal uses the digits `0` through `9`.

```text
Decimal digits:
0 1 2 3 4 5 6 7 8 9
Base: 10
```

**14:22**  Using only those ten digits, we can build numbers of any size: `90`, `100`, `200`, and so on.

**14:35**  No matter how large the decimal number is, it is composed from the same digits `0` to `9`.

**14:42–15:07**  The instructor connects the word “decimal” with the idea of ten values and explains that counting starts at zero, so the allowed digits end at nine.

### Binary

**15:13**  “Bi” means two.

**15:18**  The instructor gives the analogy of a bicycle having two wheels.

**15:26**  A tricycle has three wheels.

**15:38**  Therefore, binary is a number system based on two digits.

**15:44**  Binary represents values using only two digits:

```text
Binary digits:
0 1
Base: 2
```

**15:57**  These are often discussed as digital values.

**16:03**  In simple explanations, we often say that computers understand `0` and `1`.

**16:10**  In that sense, the computer works with binary representation.

**16:15**  If you type a decimal value such as `200`, the computer internally represents information in binary form.

**16:21–16:45**  The instructor compares this with language translation: if someone asks “How are you?” in English, you may understand its meaning in your own language, then reply. Likewise, a computer converts information into the representation it works with internally.

### Octal

**16:51**  Binary and decimal are not the only number systems. Two more being discussed are octal and hexadecimal.

**16:56**  Octal means eight.

**17:02**  The prefix relates to eight.

**17:08**  Octal uses eight digit values.

```text
Octal digits:
0 1 2 3 4 5 6 7
Base: 8
```

**17:22**  So octal representation uses digits from `0` through `7`.

**17:29**  The same written digits can look similar to decimal, so the base/notation is important.

**17:35**  When identifying an octal value mathematically, we may indicate base 8 so that it is understood as octal.

**17:43**  The Python notation for octal will be shown later.

### Hexadecimal

**17:50**  Hexadecimal is base 16.

**17:58**  It represents values using sixteen symbols.

**18:03**  The first ten are `0` through `9`.

**18:15**  Then letters are used for values ten through fifteen:

```text
A = 10
B = 11
C = 12
D = 13
E = 14
F = 15
```

**18:37**  So hexadecimal uses `0–9` and then `A–F`.

**18:43**  This is an important point, especially for beginners.

**18:50–19:17**  The instructor encourages students to watch difficult parts several times, solve the examples repeatedly, and compare homework answers with other learners.

**19:24**  Remember: hexadecimal contains sixteen symbol values from `0` through `F`.

**19:31–19:44**  Because counting begins at zero, the set `0–9` plus `A–F` gives sixteen possible digit values.

**19:49**  We do not write the hexadecimal digit values ten through fifteen as two-digit decimal strings inside a single hexadecimal digit position; we use `A–F`.

**19:55**  If Python interprets hexadecimal `A` as a numeric value and you print the integer normally, the decimal output is `10`.

**20:03**  This is again the normal human-readable decimal output.

-------------------------------------------------------------------------------
## 20:10 — TEACHING NOTE
-------------------------------------------------------------------------------

**20:10–21:45**  The instructor explains his teaching approach: a teacher should not assume that students already know basic concepts. Some students may already know the topic, some may have forgotten it, and some may be hearing the terms for the first time. Therefore, he explains the fundamentals so that technical and non-technical learners can reach the same level.

-------------------------------------------------------------------------------
## 21:50 — DECIMAL NUMBER SYSTEM IN PYTHON
-------------------------------------------------------------------------------

**21:50**  Now the instructor begins working through each number system one by one, including lab demonstrations.

**21:57**  Decimal is the first number system and is Python’s normal/default form for ordinary integer literals.

**22:04**  Decimal uses `0–9` and has base 10.

**22:10**  Because decimal is the default, we normally do not write “base 10” in Python source code.

**22:15**  Mathematically, a base can be written to clarify the number system, but ordinary Python decimal literals need no special prefix.

**22:21**  For other number systems, some identifying notation is needed.

**22:28–22:46**  The instructor explains that a base tells us how to interpret the digits; if no special base notation is given in ordinary Python integer syntax, the value is treated as decimal.

**22:53**  Example:

```python
a = 5000
```

**23:01**  Because no special prefix is used, Python treats `5000` as a decimal integer.

**23:07**  If you print it:

```python
print(a)
```

**23:14**  the output is:

```text
5000
```

**23:20**  If the same visible digits were meant as another number system, the Python notation would be different.

**23:25–24:13**  The instructor tells beginners not to jump too far ahead, jokes with the audience, and says difficult concepts should be learned gradually.

**24:13**  Another example:

```python
b = 4312
```

**24:20**  No special notation is attached to it.

**24:28**  Therefore, Python interprets it as decimal.

**24:34**  Printing it displays the same decimal value.

**24:41**  No conversion is needed because the input literal is already decimal and Python displays integers in decimal by default.

-------------------------------------------------------------------------------
## 25:00 — LAB: DECIMAL `int`
-------------------------------------------------------------------------------

**25:00**  The instructor opens Python for a lab demonstration.

**25:07**  The version shown is Python 3.11; later minor versions do not change the basic lesson.

**25:25**  Example:

```python
a = 100
```

**25:38**  Printing `a` gives:

```text
100
```

**25:45**  The displayed form is decimal.

**25:58**  We can inspect value, type, and identity together.

```python
print(a, type(a), id(a))
```

**26:05**  This shows the value, the class/data type, and the object identity.

**26:19**  Parentheses must be closed correctly when writing function calls.

**26:34**  The result shows that the value is `100`, its type is `int`, and an identity number is also displayed.

**26:46**  The identity is typically a large integer and may vary.

**26:52**  You can also check the values separately:

```python
print(type(a))
print(id(a))
```

**27:05**  Now suppose we assign a new integer:

```python
a = 500
```

**27:12**  The value associated with `a` has changed from `100` to `500`.

**27:22**  Printing it now shows `500` and its type is still `int`.

**27:29**  The identity shown by `id(a)` changes.

**27:35**  The instructor uses this to explain that integers are immutable: the reassignment refers to a different integer object rather than editing the old integer object in place.

**27:43**  Therefore, `int` is an immutable type.

**27:48**  This will be discussed in more detail later.

-------------------------------------------------------------------------------
## 28:01 — INTEGER VS FLOAT AND LARGE INTEGERS
-------------------------------------------------------------------------------

**28:01**  If you use a value containing a decimal point, it is no longer an integer. For example:

```python
b = 50.5
```

**28:08**  This is not an `int`.

**28:14**  Checking:

```python
print(type(b))
```

shows `float`.

**28:20**  The main point is that an `int` represents whole-number values rather than values with a fractional point.

**28:25**  Decimal integer literals can be written normally using digits.

**28:31**  You can use very large integer values.

**28:39**  If you incorrectly mix letters into an ordinary decimal number literal, Python will reject the syntax.

**28:46**  Python will report a syntax error for an invalid numeric literal.

**28:53**  You cannot simply attach arbitrary alphabetic characters to a decimal integer.

**28:58**  A valid integer literal must follow Python’s number syntax.

**29:04**  A large valid integer can be stored without declaring a separate `long` type.

**29:12**  Printing it returns the complete integer value.

-------------------------------------------------------------------------------
## 29:31 — BINARY NUMBER SYSTEM
-------------------------------------------------------------------------------

**29:31**  Now we move to the binary number system.

**29:50**  Binary means two. Any binary number uses only `0` and `1`.

**29:56**  Even large values can be represented using only zeros and ones.

**30:03**  The instructor says he will show how ordinary values can be represented in binary.

**30:08**  Binary has two digits and base 2.

**30:14**  A mathematical notation such as a base-2 label tells us that a sequence such as `0101` is binary.

### Python binary prefix

**30:25**  To store binary data in Python, the Python literal syntax is important.

**30:38**  If you write:

```python
a = 500
```

Python interprets it as decimal.

**30:45**  To write a binary integer literal, use the prefix `0b`.

**30:51**  The first character is zero (`0`), not the letter `O`.

**30:59**  The `b` stands for binary.

**31:06**  Example:

```python
a = 0b0101
```

**31:18**  This tells Python that the digits following `0b` are binary digits.

**31:24**  The `b` may be lowercase or uppercase:

```python
0b0101
0B0101
```

**31:31**  Both forms are valid.

**31:37**  For consistency, the instructor prefers using lowercase `0b`.

### Prefix summary

**31:57**  Binary uses `0b`.

**32:07**  Octal uses `0o` — zero followed by the letter `o`.

**32:17**  Be careful not to confuse the digit `0` with the letter `O`.

**32:23**  The `o` may be lowercase or uppercase.

**32:30**  Hexadecimal uses `0x`.

**32:38**  Therefore:

```text
Binary      -> 0b...
Octal       -> 0o...
Hexadecimal -> 0x...
```

**32:48**  This is the Python syntax for entering integer literals in those number systems.

**32:55**  If this is not clear, review it carefully because it is a basic point.

### General binary syntax

**33:07**  The general syntax is:

```text
variable_name = 0b<binary_digits>
```

**33:13**  A variable name can be any valid Python identifier.

**33:18**  `a` is only an example variable name.

**33:24**  You may use another valid identifier instead.

**33:30**  After `=`, write `0b` followed directly by the binary digits.

**33:37**  No extra mathematical base brackets are needed in Python syntax.

**33:49**  Uppercase `B` is also accepted.

**33:55**  An important question is: after you enter binary notation, what form does Python display when you print the integer?

**34:01**  The answer is: normal integer printing uses decimal output.

-------------------------------------------------------------------------------
## 34:13 — CONVERTING BETWEEN DECIMAL AND OTHER BASES
-------------------------------------------------------------------------------

**34:13**  Before continuing, the instructor explains how binary conversion works manually.

**34:24**  Consider a binary value such as `0101`.

**34:30**  Suppose we want to convert a binary value to decimal.

**34:37**  The instructor gives a rule for the manual methods used in this lesson:

```text
Other base -> Decimal : multiply digits by powers of the base and add.
Decimal -> Other base : repeatedly divide by the target base and use remainders.
```

**34:49**  From decimal to binary, octal, or hexadecimal, repeated division is used.

**35:01**  From binary/octal/hexadecimal to decimal, positional multiplication by powers of the base is used.

**35:21**  For decimal-to-binary conversion, divide by `2`.

**35:28**  For decimal-to-octal conversion, divide by `8`.

**35:33**  For decimal-to-hexadecimal conversion, divide by `16`.

-------------------------------------------------------------------------------
## 35:33 — EXAMPLE: DECIMAL 208 TO BINARY
-------------------------------------------------------------------------------

**35:33–35:47**  The instructor uses `208` as the example decimal value, although one transcript line says `2008`. The surrounding explanation and arithmetic indicate `208` is intended.

**35:52**  Because the target is binary, repeatedly divide by `2`.

**36:00**  Binary uses base 2; octal uses 8; hexadecimal uses 16.

**36:24**  Start with the decimal number and divide by `2`.

**36:37–37:20**  Continue dividing each quotient by `2` and record the remainder each time.

**37:26**  The instructor corrects himself and emphasizes the importance of the remainder.

**37:33**  When dividing by `2`, a remainder can only be `0` or `1`.

**37:50**  A remainder of `0` means the number divided evenly at that step.

**38:02**  The instructor briefly explains “remainder” using an easier example.

**38:10**  Example: `10 / 3` gives quotient `3` with remainder `1`, because `3 * 3 = 9` and `1` is left.

**38:25**  The leftover part is called the remainder.

**38:34–39:37**  Continue the repeated division by `2`, writing each remainder.

**39:48**  At the end, read the remainders from bottom to top.

**39:54**  That bottom-to-top sequence is the binary result.

**40:10**  [Music]

**40:15**  If the method feels difficult, practice the divisions yourself.

**40:20**  In Python, you do not need to do all this arithmetic manually just to interpret a binary literal; Python can calculate it immediately.

**40:27**  The manual method is being taught so you understand how the conversion works.

**40:32**  The instructor says he also knows shortcut methods, but division is a useful common method for explaining the conversions.

-------------------------------------------------------------------------------
## 40:39 — BINARY TO DECIMAL USING POWERS OF 2
-------------------------------------------------------------------------------

**40:39**  Now reverse the direction: convert a binary value to decimal.

**40:46**  Decimal-to-binary used division.

**40:53**  Binary-to-decimal uses positional multiplication by powers of `2`.

**41:12**  Example binary value:

```text
010101
```

**41:20**  The goal is to convert it into decimal.

**41:25**  Start from the rightmost digit.

**41:37**  Multiply the rightmost digit by `2^0`.

**41:52**  Move left and multiply the next digit by `2^1`.

**42:04**  Continue with `2^2`, `2^3`, and so on.

A positional expansion is therefore:

```text
(binary digit) * 2^position
```

where the rightmost position starts at `0`.

**43:12**  Any nonzero number to the power `0` equals `1`.

```text
2^0 = 1
```

**43:18**  The instructor explains this especially for non-technical learners.

**43:36**  A power/exponent tells you how many factors of the base are multiplied.

```text
2^1 = 2
2^2 = 2 * 2 = 4
2^3 = 2 * 2 * 2 = 8
2^4 = 16
2^5 = 32
```

**44:06**  Multiplying any value by zero gives zero.

**44:18**  `2^2 = 4`, and if the binary digit at that position is `1`, that position contributes `4`.

**44:32**  `2^4 = 16`; again, whether it contributes depends on whether the corresponding binary digit is `1` or `0`.

**44:49–45:09**  The instructor adds the positional values and gets a decimal result for the demonstrated binary example. The transcript around the exact written digits and arithmetic is inconsistent, so the numeric sequence is preserved as an explanation rather than silently reconstructed.

-------------------------------------------------------------------------------
## 45:31 — HOMEWORK
-------------------------------------------------------------------------------

**45:31**  The instructor gives homework to students learning Python.

**45:39**  First, practice decimal-to-binary conversion manually in your notebook, using the repeated-division method shown in the lecture.

**45:52**  Homework 1:

```text
Convert decimal 580 to binary.
```

**46:04**  Homework 2:

```text
Convert decimal 140 to binary.
```

**46:11–46:17**  Homework 3: the instructor gives a binary number to convert back to decimal, but the automatic transcript has broken the digit sequence. It should be taken directly from the original video if an exact digit-for-digit homework value is required.

**46:23**  Python can calculate the decimal value very quickly when a valid binary literal is entered with `0b...`.

**46:29**  But students should still understand the underlying conversion process.

**46:41**  If it is difficult, watch and practice the method two or three times.

**46:53**  The purpose is mainly to understand how decimal-to-binary conversion works internally/conceptually.

-------------------------------------------------------------------------------
## 47:00 — LAB: BINARY INTEGER LITERALS
-------------------------------------------------------------------------------

**47:00**  Now the instructor moves to the lab to demonstrate binary operations in Python.

**47:12**  Binary notation is still used to create values of Python type `int`.

**47:18**  A valid variable name can be chosen, for example `a`.

**47:30**  Write `0b` first, then the binary digits.

Example:

```python
a = 0b010101
```

**47:43**  Printing the value gives decimal output.

**47:49**  For the shown example, the output is `21`.

```python
print(a)
# 21
```

**47:57**  Checking the type shows that it is still `int`.

```python
print(type(a))
# <class 'int'>
```

**48:03**  You can also check `id(a)`.

**48:16**  You may print the value, type, and identity together.

```python
print(a, type(a), id(a))
```

**48:29**  This shows:

```text
stored numeric value
integer type
object identity
```

### Uppercase and lowercase binary prefix

**48:44**  The instructor used lowercase `b` in `0b`.

**48:50**  Now he tries uppercase `B`:

```python
g = 0B010101
```

**49:01**  Printing it gives the same decimal result.

**49:07**  Therefore, `0b` and `0B` are both valid.

**49:13**  There is no difference in the numeric value.

### Invalid binary digits

**49:19–49:42**  The instructor enters a longer binary literal and shows that Python still prints its decimal equivalent, even when the binary number is large.

**49:49**  Normal `print()` output remains decimal/human-readable.

**50:01**  What happens if you put the digit `2` in a binary literal?

**50:09**  Binary allows only `0` and `1`.

**50:17**  Python reports an error.

**50:24**  The error indicates that digit `2` is invalid in a binary literal.

**50:29**  So `2` cannot appear as a binary digit.

**50:34**  Likewise, arbitrary letters cannot be used in a binary literal.

**50:41**  Python rejects such invalid binary syntax.

**50:47**  Only `0` and `1` may appear as digits of a binary integer literal.

**50:53**  It is important to understand not only the valid syntax but also what error occurs when the rule is broken.

**51:00**  A syntax error occurs when the literal does not follow the required syntax/rules.

**51:12**  Python tells you that the written form is not valid binary syntax.

**51:19**  In exam questions, do not answer only “an error occurs”; know that the relevant error is a syntax error for an invalid numeric literal.

**51:32**  Invalid binary representation therefore causes a syntax error.

-------------------------------------------------------------------------------
## 51:49 — OCTAL NUMBER SYSTEM
-------------------------------------------------------------------------------

**51:49**  Decimal and binary have now been explained. The third system is octal.

**51:57**  Octal has eight possible digit values.

```text
0 1 2 3 4 5 6 7
```

**52:04**  Any octal number is built using only those digits.

**52:11**  This can initially be confusing because the digits look the same as ordinary decimal digits.

**52:17**  In Python, however, the notation is different, so the number system can be identified clearly.

**52:23**  Example digits such as `3412` can be interpreted as octal when explicitly marked as base 8.

**52:31**  If it is base 8, you should not interpret it as ordinary decimal `3412`.

**52:37**  Its decimal numeric value must be calculated separately.

**52:49**  Literals identified as base 8 are octal numbers.

### Python octal prefix

**53:01**  To store an octal literal in Python, it must start with `0o` or `0O`.

```python
a = 0o3412
```

**53:07**  The first character is zero.

**53:14**  The next character is the letter `o`.

**53:22**  Uppercase `O` is also valid:

```python
a = 0O3412
```

**53:28**  The general syntax is:

```text
variable_name = 0o<octal_digits>
```

**53:39**  For example, if you want to write octal `3412`, use:

```python
a = 0o3412
```

**53:52**  When you print it, Python gives the decimal numeric value.

-------------------------------------------------------------------------------
## 54:04 — OCTAL TO DECIMAL
-------------------------------------------------------------------------------

**54:04**  Python can calculate the value automatically, but we should understand how the conversion works manually.

**54:16**  To convert octal to decimal, use positional multiplication by powers of `8`.

**54:22**  This follows the same “other base to decimal” rule used earlier.

**54:37**  Example octal value:

```text
3412 (base 8)
```

**54:49**  Write the digits by position and start from the right-hand side.

**54:55**  The rightmost position uses `8^0`.

**55:01**  Then move left through `8^1`, `8^2`, `8^3`, etc.

The intended structure is:

```text
3 * 8^3
+ 4 * 8^2
+ 1 * 8^1
+ 2 * 8^0
```

**55:20**  Calculate each term and add them to obtain the decimal value.

**55:32–56:47**  The instructor works through the multiplication aloud. The automatic transcript contains several arithmetic-number transcription errors (for example, values around `512`, `256`, and the final total). The important method is the positional expansion above.

**56:54**  The instructor says the result will also be checked in Python to verify it.

-------------------------------------------------------------------------------
## 57:06 — DECIMAL TO OCTAL
-------------------------------------------------------------------------------

**57:06**  To convert in the opposite direction — decimal to octal — use repeated division.

**57:16**  Octal-to-decimal used multiplication; decimal-to-octal uses division.

**57:22**  Because the target base is octal, divide repeatedly by `8`.

**57:30–58:21**  Record each remainder after division by `8`.

**58:21**  Read the remainders from bottom to top to obtain the octal representation.

**58:26–58:37**  The instructor states that the result matches the earlier octal example, using it as verification of the method.

**58:43**  The next step is to verify the notation and conversion in Python.

-------------------------------------------------------------------------------
## 58:55 — LAB: OCTAL INTEGER LITERALS
-------------------------------------------------------------------------------

**58:55**  The instructor opens the lab for octal values.

**59:01**  Octal integer literals use `0o`.

```python
a = 0o<digits_0_to_7>
```

**59:08**  The `o` can be lowercase or uppercase.

**59:13**  After `0o`, only octal digits `0` through `7` are allowed.

**59:20**  Python calculates the numeric value and `print()` displays it in decimal.

**59:28–59:35**  The instructor prints an example and receives a decimal output.

**59:40**  He returns to the earlier example `3412`.

**59:45**  He corrects himself from saying `0b` and uses octal `0O`/`0o` instead.

### Distinguishing zero `0` from the letter `O`

**59:53**  The instructor points out a visual difference in the font: the digit zero may contain a dot, while the letter `O` may not.

**1:00:01**  This can help you distinguish `0` from `O` in code or printed material, depending on the font.

**1:00:08**  Remember that Python’s octal prefix begins with the digit zero, followed by the letter `o`.

**1:00:22**  Example:

```python
b = 0O3412
```

**1:00:28–1:00:41**  Printing the value gives the corresponding decimal value, which the instructor compares with the board calculation.

**1:00:48**  Checking `type(b)` still gives `int`.

**1:00:53**  Checking `id(b)` gives an object identity value.

### Invalid octal digits

**1:01:06**  The instructor tries another octal value.

**1:01:13**  He asks whether digit `8` can be used in an octal literal.

**1:01:19**  Octal allows only `0` through `7`.

**1:01:26**  Therefore `8` is invalid in an octal literal.

**1:01:32**  Python reports a syntax error for an invalid octal digit.

**1:01:40–1:02:18**  The instructor experiments with valid and invalid octal forms, reinforcing that only digits `0–7` may follow an octal prefix and that lowercase/uppercase `o` both work.

-------------------------------------------------------------------------------
## 1:02:xx — HEXADECIMAL NUMBER SYSTEM
-------------------------------------------------------------------------------

**Around 1:02–1:03**  The instructor moves to the fourth number system: hexadecimal.

Hexadecimal has base 16 and uses:

```text
0 1 2 3 4 5 6 7 8 9 A B C D E F
```

with:

```text
A = 10
B = 11
C = 12
D = 13
E = 14
F = 15
```

### Python hexadecimal prefix

Use:

```python
0x...
```

or uppercase `X`:

```python
0X...
```

The letters `A–F` inside the hexadecimal digits can also be lowercase or uppercase.

-------------------------------------------------------------------------------
## 1:04–1:07 — DECIMAL AND HEXADECIMAL CONVERSION
-------------------------------------------------------------------------------

**Around 1:04**  To convert hexadecimal to decimal, multiply each digit value by a power of `16`, starting with `16^0` at the rightmost digit.

General pattern:

```text
... + digit * 16^2 + digit * 16^1 + digit * 16^0
```

**Around 1:05:03**  To convert decimal to hexadecimal, repeatedly divide by `16`.

**1:05:08**  The instructor uses decimal `200` as an example.

**1:05:17**  Divide `200` by `16`. The quotient/remainder process leaves a remainder of `8` at one step.

**1:05:23**  Continue until the quotient is smaller than `16`.

**1:05:29**  If a remaining hexadecimal digit has decimal value `12`, do not write the two characters `12` as one hex digit.

**1:05:34**  Hexadecimal value `12` is represented by `C`.

**1:05:40**  Therefore decimal `200` becomes hexadecimal `C8`.

```text
200 decimal = C8 hexadecimal
```

**1:05:45**  In Python:

```python
a = 0xC8
print(a)
```

**1:05:52**  Normal output is:

```text
200
```

### Hexadecimal `C8` back to decimal

**1:06:00**  Now reverse the conversion.

**1:06:08**  Write `C8` by positions, starting from the right.

**1:06:14**  The rightmost `8` uses `16^0`.

**1:06:21**  `C` is in the next position, so it uses `16^1`.

```text
C8(hex)
= C * 16^1 + 8 * 16^0
= 12 * 16 + 8 * 1
= 192 + 8
= 200
```

**1:07:01**  This verifies both directions: decimal-to-hexadecimal and hexadecimal-to-decimal.

**1:07:08**  The method remains the same for larger numbers.

**1:07:13**  When using the repeated-division method, read the remainders from bottom to top.

**1:07:20**  If a remainder is `12`, write `C`, not decimal characters `12`, because one hexadecimal digit represents values `0–15`.

### Invalid hexadecimal characters

**1:07:32**  What if you use a letter beyond `F`, such as `H`?

**1:07:38**  Python cannot interpret it as a hexadecimal digit.

**1:07:43**  Hexadecimal digit letters stop at `F`.

**1:07:49**  A character beyond the valid set makes the literal invalid and produces an error.

-------------------------------------------------------------------------------
## 1:08:03 — LAB: HEXADECIMAL INTEGER LITERALS
-------------------------------------------------------------------------------

**1:08:03**  Now the instructor demonstrates hexadecimal in Python.

**1:08:08**  Hexadecimal notation still creates an integer value.

**1:08:13**  Use the prefix `0x`. Lowercase `x` or uppercase `X` is accepted.

**1:08:20**  Valid hexadecimal digits range from `0` through `F`.

**1:08:27**  These are:

```text
0 1 2 3 4 5 6 7 8 9 A B C D E F
```

**1:08:34**  The instructor first tries an example with the digit sequence `0101` in hexadecimal notation.

**1:08:43**  Printing it returns the decimal equivalent.

**1:08:48**  The same visible digit sequence has different numeric values when interpreted under different bases.

**1:08:53**  Therefore, binary `0101`, octal `0101`, and hexadecimal `0101` do not all mean the same decimal value.

**1:09:00**  The transcript records an example output of `65793` for one shown hexadecimal value.

**1:09:06**  The instructor then uses uppercase `X` to show that case does not matter for the prefix.

**1:09:12**  He uses hexadecimal letters such as `A` and `C` in another example.

**1:09:25**  Python accepts `A` and `C` because they are valid hexadecimal digits.

**1:09:30**  The transcript records a decimal result of `2754` for that demonstrated value.

### Letter case in hexadecimal

**1:09:36**  The instructor asks whether hexadecimal letters can be uppercase.

**1:09:43**  He creates another variable with uppercase hexadecimal letters.

**1:09:48**  Printing gives the same numeric value.

**1:09:55**  Therefore, hexadecimal digit letters are case-insensitive.

**1:10:00**  Lowercase and uppercase `A–F` are both accepted.

**1:10:05**  This is an important point.

**1:10:12**  The prefix may also be `0x` or `0X`.

### More hexadecimal examples

**1:10:17**  Another hexadecimal value is assigned using `0x...`.

**1:10:24**  The instructor uses several valid hexadecimal characters.

**1:10:29**  He reminds students of the values:

```text
A = 10
C = 12
E = 14
F = 15
```

**1:10:44**  Python prints the decimal equivalent.

**1:10:50**  The transcript records a decimal output of `64206` for the demonstrated literal.

### Invalid character example

**1:10:56**  The instructor then enters a hexadecimal literal containing a character outside the allowed hexadecimal set.

**1:11:05**  Because that character is not valid hexadecimal, Python reports a syntax error.

**1:11:11**  Any alphabetic hexadecimal digit must be within `A–F` (or lowercase `a–f`).

**1:11:18**  Other letters are invalid in a hexadecimal integer literal.

**1:11:23**  Therefore, valid letter characters are limited to:

```text
A B C D E F
```

**1:11:29**  You may use any valid combination of those letters and the digits `0–9`.

**1:11:36**  The instructor stores another valid hexadecimal value in a variable and prints it.

**1:11:47**  Python returns its decimal equivalent.

**1:11:52**  No error occurs because all characters belong to the valid hexadecimal set.

**1:11:59**  If you use characters outside that set, an error is expected.

**1:12:07**  Numeric digits `0–9` are valid hexadecimal digits.

**1:12:14**  Values ten through fifteen are represented by letters rather than by writing `10`, `11`, `12`, etc. as single hexadecimal digits.

-------------------------------------------------------------------------------
## 1:12:38 — ALL THESE FORMS ARE STILL `int`
-------------------------------------------------------------------------------

**1:12:38**  The instructor checks the data type of a hexadecimal example.

**1:12:46**  `type(...)` shows `int`.

**1:12:52**  `id(...)` can also be checked.

**1:12:59**  Whether an integer literal is written in binary, octal, decimal, or hexadecimal notation, the resulting Python numeric object is still of type `int`.

```text
Decimal literal      -> int
Binary literal       -> int
Octal literal        -> int
Hexadecimal literal  -> int
```

-------------------------------------------------------------------------------
## 1:13:05 — EXAM / ERROR POINTS
-------------------------------------------------------------------------------

**1:13:05**  The instructor hopes the `int` data type is now clear.

**1:13:11**  Exam questions may ask what happens when an invalid digit is used in a number-system literal.

**1:13:18**  Remember the error category discussed in the lecture: a syntax error occurs for an invalid numeric literal.

**1:13:23**  In other words, if you place a digit/character that does not exist in that number system, the literal is invalid.

Examples:

```python
0b102      # invalid: binary allows only 0 and 1
0o128      # invalid: octal allows only 0 to 7
0x12H      # invalid: hexadecimal allows only 0-9 and A-F/a-f
```

-------------------------------------------------------------------------------
## 1:13:29 — WHAT REMAINS FOR THE NEXT LECTURE
-------------------------------------------------------------------------------

**1:13:29**  The instructor says the main topic for today is complete.

**1:13:35**  One small part remains: direct base conversion between non-decimal systems, such as binary to octal and octal to hexadecimal.

**1:13:42**  That will be taught in the next lecture so that this lecture does not become too long and difficult to digest.

**1:13:50**  Students are asked to watch the playlist in sequence.

**1:13:55**  If a lecture seems missing, check the complete playlist because the lectures are arranged there in order.

**1:14:00**  Learn how to open and follow playlists on the YouTube channel.

**1:14:05**  The instructor also mentions the lecture number in each video to reduce confusion.

-------------------------------------------------------------------------------
## 1:14:12 — CLOSING POETRY AND SOCIAL LINKS
-------------------------------------------------------------------------------

**1:14:12**  As usual, the instructor ends with a poem/couplet and mentions Bashir Badr.

**1:14:19–1:14:44**  The approximate meaning of the quoted lines is:

```text
Pray that this plant always appears green;
Even in sadness, may the face continue to look bright.

What a strange person — even when upset, he smiles;
I want it to be clear when he is truly angry.
```

> Note: The automatic transcript is imperfect in this poetic section, so this is a meaning-focused English rendering rather than a claim of exact poetic wording.

**1:14:50**  The instructor says these were a few lines from the ghazal and asks viewers to take care.

**1:14:55**  He mentions that his Instagram and LinkedIn links are shown after the video.

**1:15:02**  Viewers can follow him on Instagram or LinkedIn, and other links are also available there.

**1:15:09**  Take care, and remember me in your prayers. [Music]

-------------------------------------------------------------------------------
# ASCII QUICK REFERENCE
-------------------------------------------------------------------------------

```text
+---------------+--------+-----------------------+----------------+
| Number System | Base   | Allowed Digits        | Python Prefix  |
+---------------+--------+-----------------------+----------------+
| Decimal       | 10     | 0-9                   | none           |
| Binary        | 2      | 0, 1                  | 0b or 0B       |
| Octal         | 8      | 0-7                   | 0o or 0O       |
| Hexadecimal   | 16     | 0-9, A-F / a-f        | 0x or 0X       |
+---------------+--------+-----------------------+----------------+
```

```text
+--------------------------+-------------------------------------------+
| Built-in                 | Purpose                                   |
+--------------------------+-------------------------------------------+
| print(x)                 | Display the value/output of x             |
| type(x)                  | Show the class/data type of x             |
| id(x)                    | Show the identity value of the object     |
+--------------------------+-------------------------------------------+
```

```text
+--------------------------------+--------------------------------------+
| Conversion Direction           | Manual Method                        |
+--------------------------------+--------------------------------------+
| Binary -> Decimal              | Multiply by powers of 2 and add      |
| Octal -> Decimal               | Multiply by powers of 8 and add      |
| Hexadecimal -> Decimal         | Multiply by powers of 16 and add     |
| Decimal -> Binary              | Repeatedly divide by 2               |
| Decimal -> Octal               | Repeatedly divide by 8               |
| Decimal -> Hexadecimal         | Repeatedly divide by 16              |
+--------------------------------+--------------------------------------+
```

-------------------------------------------------------------------------------
# CORE PYTHON EXAMPLES
-------------------------------------------------------------------------------

```python
# Decimal integer
x = 100
print(x)            # 100
print(type(x))      # <class 'int'>
print(id(x))        # identity value varies

# Float, not int
f = 50.5
print(type(f))      # <class 'float'>

# Binary
b = 0b010101
print(b)            # 21
print(type(b))      # <class 'int'>

# Octal
# Only digits 0-7 are valid after 0o / 0O
o = 0o3412
print(o)            # decimal equivalent
print(type(o))      # <class 'int'>

# Hexadecimal
h = 0xC8
print(h)            # 200
print(type(h))      # <class 'int'>
```

-------------------------------------------------------------------------------
# IMPORTANT EXAM POINTS
-------------------------------------------------------------------------------

```text
1. `int` represents whole/integral values.
2. Python 3 has no separate explicit `long` integer type.
3. Ordinary integer output from `print()` is decimal by default.
4. Binary literals use 0b / 0B and digits 0-1 only.
5. Octal literals use 0o / 0O and digits 0-7 only.
6. Hexadecimal literals use 0x / 0X and digits 0-9 plus A-F/a-f.
7. Binary, octal, decimal, and hexadecimal integer literals all produce Python `int` values.
8. Invalid digits/letters in a numeric literal produce a syntax error.
9. For manual conversion to decimal, use positional powers of the source base.
10. For manual conversion from decimal to another base, repeatedly divide by the target base and read remainders from bottom to top.
11. Integers are immutable; reassigning a variable to another integer can produce a different object identity.
```

-------------------------------------------------------------------------------
# HOMEWORK FROM THE LECTURE
-------------------------------------------------------------------------------

```text
Q1. Convert decimal 580 to binary.
Q2. Convert decimal 140 to binary.
Q3. Convert the binary value given in the original video to decimal.
    Note: the digit sequence for Q3 is corrupted in the automatic transcript.
```

-------------------------------------------------------------------------------
# END OF TRANSLATION
-------------------------------------------------------------------------------
