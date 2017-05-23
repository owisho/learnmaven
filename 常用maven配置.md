### 常用maven配置

```
<build>  
    <pluginManagement>    
        <plugins>   
            <!-- 编译插件 -->    
            <plugin>   
	        <groupId>org.apache.maven.plugins</groupId>    
	        <artifactId>maven-compiler-plugin</artifactId>    
	        <version>3.6.1</version>    
	        <configuration>    
	            <source>1.7</source>    
		    <target>1.7</target>   
	        </configuration>   
	    </plugin>     
	    <!-- 资源文件插件 -->    
            <plugin>   
		<groupId>org.apache.maven.plugins</groupId>   
		<artifactId>maven-resources-plugin</artifactId>
		<version>3.0.2</version>
		<configuration>   
		    <encoding>UTF-8</encoding>   
	        </configuration>   
	    </plugin> 
	    <!-- 源码文件插件 -->     
	    <plugin>    
		<groupId>org.apache.maven.plugins</groupId>     
		<artifactId>maven-source-plugin</artifactId>    
		<version>3.0.1</version>    	
		<executions>          
		    <execution>         
		        <id>attach-sources</id>  
			<phase>verify</phase>
			<goals>
			    <goal>jar-no-fork</goal>
			</goals>
		    </execution>
	        </executions>
	    </plugin>
	    <!-- 测试插件 -->
	    <plugin>
	        <groupId>org.apache.maven.surefire</groupId>
		<artifactId>surefire-junit47</artifactId>
		<version>2.20</version>
		<configuration>
          	    <parallel>methods</parallel>
          	    <threadCount>10</threadCount>
        	</configuration>
	    </plugin>
        </plugins>   
    <pluginManagement>    
</build>   
```
