# Chapter 1 引言

1. JSP

    > Java Server Pages    

2. Servlet

    > servlet
    
3. JSP & Servlet
    
    > JSP 的本质是 Servlet， Servlet 的本质是 Class

4. 环境配置
    - 应用服务器
        - <a href="../doc/the-great-java-app-server-debate.pdf" target="_blank">[PDF] the great java app server debate</a>
    - JSP 和 Servlet 的 Container 容器
    - Tomcat
    
        ![tomcat](../image/tomcat.png)

        - unzip apache-tomcat-7.0.65-windows-x86 to your_tomecat_directory
        - Windows
            - set environment variable:
                
                your_tomcat_directory/bin/setclasspath.bat
            
                ```
                set JAVA_HOME=your_jdk_directory
                ```
            
            - run or shutdown:
                
                your_tomcat_directory/bin/
                
                ```
                startup.bat
                
                or
                
                shutdown.bat
                ```
            
        - browser:
        
            ```
            localhost:8080
            127.0.0.1:8080
            your_ip:8080
            ```

5. JSP Hello,world！
6. HTTP(s)

    > Hyper Text Transfer Protocol 超文本传输协议
