
**StringBuffer :**


➤ StringBuffer is a class in Java used when we want to work with strings that change frequently.

➤ Normal strings (String class) are immutable, meaning once created, they cannot be changed.

➤ Every time we modify a String, a new object is created, which can waste memory and reduce performance.

➤ StringBuffer solves this by allowing mutable strings, so we can modify the same object without creating a new one.

➤ It supports operations like append(), insert(), delete(), and reverse() to manipulate text.

➤ *Example -* StringBuffer sb = new StringBuffer("Hello"; sb.append("World"); → HelloWorld

➤ StringBuffer is thread-safe, meaning multiple threads cannot access the same object simultaneously without synchronization.

➤ Because of synchronization, it is slower than StringBuilder.

➤ It is very useful in multi-threaded applications where data safety is more important than speed.


