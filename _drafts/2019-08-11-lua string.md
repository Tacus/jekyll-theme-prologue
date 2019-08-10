---
textarea: lua string

---
**Chapter 4. Strings**

Strings represent text. A string in Lua can contain a single letter or an entire book. Programs that manip- ulate strings with 100K or 1M characters are not unusual in Lua.

Strings in Lua are sequences of bytes. The Lua core is agnostic about how these bytes encode text. Lua is eight-bit clean and its strings can contain bytes with any numeric code, including embedded zeros. This means that we can store any binary data into a string. We can also store Unicode strings in any representation (UTF-8, UTF-16, etc.); however, as we will discuss, there are several good reasons to use UTF-8 whenever possible. The standard string library that comes with Lua assumes one-byte characters, but it can handle UTF-8 strings quite reasonably. Moreover, since version 5.3, Lua comes with a small library to help the use of UTF-8 encoding.

Strings in Lua are immutable values. We cannot change a character inside a string, as we can in C; instead, we create a new string with the desired modifications, as in the next example:

                  a = "one string"
                  b = string.gsub(a, "one", "another")  -- change string parts
                  print(a)       --> one string
                  print(b)       --> another string
    

Strings in Lua are subject to automatic memory management, like all other Lua objects (tables, functions, etc.). This means that we do not have to worry about allocation and deallocation of strings; Lua handles it for us.

Strings 代表文本。在lua中一个string 可以包含一个字母，或者整本书。在程序里面维护一个100k或者1m的字符是非常常用的。

Strings在lua中是字节序列。lua 核心并不知道这个字节怎么编码成文本。lua是