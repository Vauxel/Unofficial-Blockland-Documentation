# Strings

**A string is a sequence of characters (letters, numerical digits, punctuation marks, whitespace, and control characters).**

## Parsing
----------

### **strCmp**
*Compares **%one** and **%two** in [lexicographical order](https://en.wikipedia.org/wiki/Lexicographical_order) <u>with</u> case-sensitivity.*

* `Parameters` - string **%one**, string **%two**
* `Returns` - `0` if strings **%one** and **%two** are equal, `-1` if **%one** precedes **%two** lexicographically, and `1` if **%one** comes after **%two** lexicographically.

```csharp
==> strCmp("Blockland", "Blockland");
0
==> strCmp("Blockland", "Brickland"); // 'l' < 'r'
-1
==> strCmp("Blockland", "Badspot"); // 'l' > 'a'
1
```

### **striCmp**
*Functions the same way as **strCmp**, but instead compares **%one** and **%two** in [lexicographical order](https://en.wikipedia.org/wiki/Lexicographical_order) <u>without</u> case-sensitivity.*

* `Parameters` - string **%one**, string **%two**
* `Returns` - `0` if strings **%one** and **%two** are equal, `-1` if **%one** precedes **%two** lexicographically, and `1` if **%one** comes after **%two** lexicographically.

### **strPos**
*Searches for the position of the character(s) **%needle** in the string, **%hay**, <u>with</u> case-sensitivity.*

* `Parameters` - string **%hay**, string **%needle**, integer **%offset** *(optional)*
* `Returns` - The index of **%needle** in **%hay**, and `-1` if **%needle** could not be found in **%hay**.

```csharp
==> strPos("Test", "t");
3
```

### **striPos**
*Searches for the position of the character(s) **%needle** in the string, **%hay**, <u>without</u> case-sensitivity.*

* `Parameters` - string **%hay**, string **%needle**, integer **%offset** *(optional)*
* `Returns` - The index of **%needle** in **%hay**, and `-1` if **%needle** could not be found in **%hay**.

```csharp
==> striPos("Test", "t");
0
```

### **strLen**
*Counts the total number of characters in **%string**.*

* `Parameters` - string **%string**
* `Returns` - An integer representing the total number of characters in **%string**.

```csharp
==> strLen("Example");
7
```

### **getCharCount**
*Counts the number of times the character **%char** appears in **%string**.*

* `Parameters` - string **%string**, char **%char**
* `Returns` - An integer representing the number of times **%char** was found in **%string**.

```csharp
==> getCharCount("example", "e");
2
```

## Processing
-------------

### **strChr**
*Extracts the characters following the first instance of **%char** in **%string**, including the **%char** itself.*

* `Parameters` - string **%string**, char **%char**
* `Returns` - String containing the characters located at and after the first appearance of the **%char** given in **%string**.  If the **%char** specified could not be found in the **%string**, the whole string is returned un-modified.

```csharp
==> strChr("Hello World!", "W");
"World!"
```

### **getSubStr**
*Extracts characters in **%string**, starting at the index, **%start**, and ending after **%numChars** have been read.*

* `Parameters` - string **%string**, integer **%start**, integer **%numChars**
* `Returns` - String containing the characters in **%string** located at and after **%start**, stopping after the amount specified in **%numberChars** have been read.

```csharp
==> getSubStr("Hello World!", 0, 5);
"Hello"
```

### **strReplace**
*Replaces all instances of **%from** in **%source** with **%to**.*

* `Parameters` - string **%source**, string **%from**, string **%to**
* `Returns` - Copy of **%string** which has all of the characters in **%from** replaced by the characters in **%to**.

```csharp
==> strReplace("Blockhead built a town", "town", "castle");
"Blockhead built a castle"
```

### **stripChars**
*Removes all instances of **%chars** from **%string**.*

* `Parameters` - string **%string**, string **%chars**
* `Returns` - String containing all of the characters, except the ones from **%chars**, given in **%string**.

```csharp
==> stripChars("a1b2c3d4", "1234");
"abcd"
```

### **stripMLControlChars**
*Removes all instances of [Torque Markup Language](./tml.md) characters from **%string**.*

* `Parameters` - string **%string**
* `Returns` - String containing all of the characters, except [TML](./tml.md) characters, given in **%string**.

### **stripTrailingSpaces**
*Removes all spaces following the last non-space character in **%string***

* `Parameters` - string **%string**
* `Returns` - **%string** with trailing spaces omitted.

```csharp
==> stripTrailingSpaces("Blockland  ");
"Blockland"
```

### **ltrim**
*Removes all whitespace located before the first non-whitespace character in **%string***

* `Parameters` - string **%string**
* `Returns` - **%string** with preceding whitespace omitted.

```csharp
==> ltrim("    1234");
"1234"
```

### **rtrim**
*Removes all whitespace located after the last non-whitespace character in **%string***

* `Parameters` - string **%string**
* `Returns` - **%string** with trailing whitespace omitted.

```csharp
==> rtrim("1234    ");
"1234"
```

### **trim**
*Removes all whitespace located before and after the first and last non-whitespace character in **%string***

* `Parameters` - string **%string**
* `Returns` - **%string** with preceding and trailing whitespace omitted.

```csharp
==> trim("    1234    ");
"1234"
```

### **strUrp**
*Converts all lowercase alphabetical characters in **%string** to their uppercase equivalents.*

* `Parameters` - string **%string**
* `Returns` - String containing all characters in **%string** converted to uppercase.

```csharp
==> strUrp("the quick brown fox jumps over the lazy dog");
"THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG"
```

### **strLwr**
*Converts all uppercase alphabetical characters in **%string** to their lowercase equivalents.*

* `Parameters` - string **%string**
* `Returns` - String containing all characters in **%string** converted to lowercase.

```csharp
==> strLwr("THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG");
"the quick brown fox jumps over the lazy dog"
```

### **expandEscape**
*Adds another escape level to escape characters.*

* `Parameters` - string **%text**
* `Returns` - String containing all the characters in **%text**, with the escaped characters being further escaped.

```csharp
==> expandEscape("Test\n");
"Test\\n"
```

### **collapseEscape**
*Removes an escape level from the escaped escape characters.*

* `Parameters` - string **%text**
* `Returns` - String containing all the characters in **%text**, with the escaped characters being unescaped one level.

```csharp
==> collapseEscape("Test\\n");
"Test\n"
```

### **deTag**
*Converts a tagged string to a normal string.*

* `Parameters` - string **%tagged**
* `Returns` - String containing the untagged conversion of **%tagged**.

```csharp
==> deTag('leet');
"leet"
```

*Note: You can only detag a string that has already been transmitted to you.*

### **getTag**
*Gets the tagged number associated with a tagged string*

* `Parameters` - string **%tagged**
* `Returns` - Integer representing the tagged string, **%tagged**.

```csharp
==> getTag('leet');
<somenumber>
```

## Words
--------

### **getWordCount**
*Counts the number of words that appear in the string **%text**.*

* `Parameters` - string **%text**
* `Returns` - An integer representing the number of words in **%string**.

```csharp
==> getWordCount("Hello World");
2
```

### **getWord**
*Captures the word in **%string** located at the integer index **%index**.*

* `Parameters` - string **%text**, integer **%index**
* `Returns` - String containing the characters of the word found at **%index** in **%string**.  Returns an empty string if a word could not be found at the specified **%index**.

```csharp
==> getWord("Hello World", 0);
"Hello"
```

### **getWords**
*Captures the word(s) in **%string** located at the integer index **%index**, and optionally ending at the integer index **%endIndex**.*

* `Parameters` - string **%text**, integer **%index**, integer **%endIndex**
* `Returns` - String containing the characters of the word(s) found at and between **%index** and **%endIndex** in **%string**.  Returns an empty string if a word/words could not be found at the **%index**.

```csharp
==> getWords("Hello World, how are you?", 2, 4);
"how are you?"
```

### **setWord**
*Replaces the word in **%string** located at the integer index **%index** with the string, **%replace**.*

* `Parameters` - string **%text**, integer **%index**, string **%replace**
* `Returns` - A replica of **%string** with the word at **index** replaced with the string, **%replace**.

```csharp
==> setWord("Hello World", "Hello", "Hey");
"Hey World"
```

### **removeWord**
*Removes the word in **%string** located at the integer index **%index**.*

* `Parameters` - string **%text**, integer **%index**
* `Returns` - A replica of **%string** with the word at **index** removed.

```csharp
==> removeWord("Hello World", "Hello");
"World"
```

### **firstWord**
*Captures the first word that appears in **%text**.*

* `Parameters` - string **%text**
* `Returns` - String containing the characters of the first word found in **%text**.

```csharp
==> firstWord("Hello World");
"Hello"
```

### **restWords**
*Captures every word in **%text** except the first.*

* `Parameters` - string **%text**
* `Returns` - String containing the characters of the word(s) found after the first word in **%string**.  Returns an empty string if there are not any words after the first.

```csharp
==> restWords("Hello World, how are you?");
"World, how are you?"
```

## Fields
---------

*'^' characters represent field delimiters.*

### **getFieldCount**
*Counts the number of fields that appear in the string **%text**.*

* `Parameters` - string **%text**
* `Returns` - An integer representing the number of fields in **%string**.

```csharp
==> getFieldCount("Foo^Bar");
2
```

### **getField**
*Captures the field in **%string** located at the integer index **%index**.*

* `Parameters` - string **%text**, integer **%index**
* `Returns` - String containing the characters of the field found at **%index** in **%string**.  Returns an empty string if a field could not be found at the specified **%index**.

```csharp
==> getField("Foo^Bar", 0);
"Foo"
```

### **getFields**
*Captures the field(s) in **%string** located at the integer index **%index**, and optionally ending at the integer index **%endIndex**.*

* `Parameters` - string **%text**, integer **%index**, integer **%endIndex**
* `Returns` - String containing the characters of the field(s) found at and between **%index** and **%endIndex** in **%string**.  Returns an empty string if a field/fields could not be found at the **%index**.

```csharp
==> getFields("Foo^Bar^Baz^Qux", 2, 3);
"Baz^Qux"
```

### **setField**
*Replaces the field in **%string** located at the integer index **%index** with the string, **%replace**.*

* `Parameters` - string **%text**, integer **%index**, string **%replace**
* `Returns` - A replica of **%string** with the field at **index** replaced with the string, **%replace**.

```csharp
==> setField("Foo^Bar^Baz^Qux", 0, "Hello");
"Hello^Foo^Baz^Qux"
```

### **removeField**
*Removes the field in **%string** located at the integer index **%index**.*

* `Parameters` - string **%text**, integer **%index**
* `Returns` - A replica of **%string** with the field at **index** removed.

```csharp
==> removeField("Foo^Bar^Baz^Qux", 3);
"Foo^Bar^Baz"
```

### **firstField**
*Captures the first field that appears in **%text**.*

* `Parameters` - string **%text**
* `Returns` - String containing the characters of the first field found in **%text**.

```csharp
==> firstField("Foo^Bar^Baz^Qux");
"Foo"
```

### **restFields**
*Captures every field in **%text** except the first.*

* `Parameters` - string **%text**
* `Returns` - String containing the characters of the field(s) found after the first field in **%string**.  Returns an empty string if there are not any fields after the first.

```csharp
==> restFields("Foo^Bar^Baz^Qux");
"Bar^Baz^Qux"
```