# JDK 11
参阅 https://openjdk.java.net/projects/jdk/11/

## 目录
- 单Java源文件直接运行
  ```bash
  HelloWorld.java
  ```
- 集合新方法of() since JDK 9+
- DiamondOperator<> 加强
- Files新方法
  - Files.writeString()
  - Files.readString()
  - Files.delete()
- 本地变量用于Lambda参数：(var s1, var s2) -> s1 + s2
- String新方法
  - lines();
  - isBlank();
  - stripLeading();
  - stripTrailing();
  - strip();
  - repeat();
- TimeUnit新转化方法 TimeUnit.DAYS.convert
- HTTP Client (Standard)
- Nested Based Access Control
  ```jav
  public class Main {
      public void myPublic() {
      }
      private void myPrivate() {
      }
      class Nested {
          public void nestedPublic() {
              myPrivate();
          }
      }
  }
  ```
  we use Java Reflection, it will give an IllegalStateException
  ```
  Method method = ob.getClass().getDeclaredMethod("myPrivate");
  method.invoke(ob);
  ```
- JEP 329: ChaCha20 and Poly1305 Cryptographic Algorithms

  Java 11 provides ChaCha20 and ChaCha20-Poly1305 cipher implementations. These algorithms will be implemented in the SunJCE provider.
  
- JEP 333: ZGC: A Scalable Low-Latency Garbage Collector (Experimental)