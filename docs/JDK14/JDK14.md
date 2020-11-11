# JDK 14

## 目录
- Switch Expressions
- Helpful NullPointerExceptions

  Before Java 14
  ```
  String name = jd.getBlog().getAuthor()
   
  //Stacktrace
  Exception in thread "main" java.lang.NullPointerException
      at NullPointerExample.main(NullPointerExample.java:5)
  ```
  
  After Java 14
  ```
  Exception in thread "main" java.lang.NullPointerException: Cannot invoke "Blog.getAuthor()" 
  because the return value of "Journaldev.getBlog()" is null
    at NullPointerExample.main(NullPointerExample.java:4)
  ```
