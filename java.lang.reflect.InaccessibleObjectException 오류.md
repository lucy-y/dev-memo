```
java.lang.reflect.InaccessibleObjectException-->Unable to make protected final java.lang.Class java.lang.ClassLoader.defineClass
```
Java | Unable to make protected final java.lang.Class java.lang.ClassLoader.defineClass 해결하는 방법
Java9 버전 이후부터는 reflection API 관련 기능에 제한이 있음

JVM Arguments에 
```
--add-opens=java.base/java.lang=ALL-UNNAMED 
```
선언해주고 빌드하여 개발

### 참고
- https://cojun.tistory.com/177
- https://yian.tistory.com/53
