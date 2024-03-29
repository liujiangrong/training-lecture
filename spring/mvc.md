# Chapter 3 Spring MVC

1. update build.gradle

    ```
    compile 'commons-fileupload:commons-fileupload:1.3.1'
    compile 'org.springframework:spring-webmvc:4.2.4.RELEASE'
    ```

2. update web.xml

    ```xml
    <!-- Spring DispatcherServlet -->
    <servlet>
        <servlet-name>web</servlet-name>
        <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
    </servlet>
    <!-- mapping -->
    <servlet-mapping>
        <servlet-name>web</servlet-name>
        <url-pattern>/</url-pattern>
    </servlet-mapping>
    
    <!-- Spring ContextLoaderListener -->
    <listener>
    <listener-class>org.springframework.web.context.ContextLoaderListener</listener-class>
    </listener>
    
    <!-- Spring applicationContext.xml Location -->
    <context-param>
        <param-name>contextConfigLocation</param-name>
        <param-value>classpath:applicationContext.xml</param-value>
    </context-param>
    ```

3. create WEB-INF/DispatcherServlet_name-servlet.xml

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <beans xmlns="http://www.springframework.org/schema/beans"
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:context="http://www.springframework.org/schema/context"
           xmlns:mvc="http://www.springframework.org/schema/mvc"
           xsi:schemaLocation="
           http://www.springframework.org/schema/beans
           http://www.springframework.org/schema/beans/spring-beans.xsd
           http://www.springframework.org/schema/context
           http://www.springframework.org/schema/context/spring-context.xsd
           http://www.springframework.org/schema/mvc
           http://www.springframework.org/schema/mvc/spring-mvc.xsd">
    
        <mvc:annotation-driven />
        <context:component-scan base-package="controller" />
    
        <bean id="multipartResolver" class="org.springframework.web.multipart.commons.CommonsMultipartResolver"/>
        <bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
            <property name="prefix" value="/"/>
            <property name="suffix" value=".jsp"/>
        </bean>
    </beans>
    ```

4. create Controller
    
    ```java
    @Controller
    @RequestMapping("/user")
    public class UserController {
    
        @RequestMapping("/add")
        private void add() {
            // ...
            System.out.println("add...");
        }
    }
    ```