### Maven坐标:</br>
groupId,artifactedId,version,packaging,classifier(用来帮助定义构建输出的一些附属构件。</br>
附属构件与主构件对应，如nexus-indexer-2.0.0.jar，这个项目可能通过使用一些插件生成如</br>
nexus-indexer-2.0.0-javadoc.jar,nexus-indexer-2.0.0-sources.jar这样一些附属构件，其中</br>
包含了Java文档和源代码。这时候，javadoc和sources就是这两个附属构件的classifier。这样，附属构件</br>
也就拥有了自己唯一的坐标。注意，不能直接定义自己项目的classifier，因为附属构件不是项目直接默认生成</br>
的，而是由附加的插件帮助生成)

### 三套生命周期  
#### clean生命周期  
pre-clean  
clean  
post-clean  
#### default生命周期  
validate  
initialize  
generate-sources  
process-sources  处理项目主资源文件。src/main/resources目录内容    
generate-resources  
process-resources  
compile  编译项目的主源码。src/main/java目录下的内容编译到主classpath目录中    
process-class  
generate-test-sources  
process-test-sources  处理项目测试资源文件。src/test/resources目录内容    
generate-test-resources  
process-test-resources  
test-compile  编译项目测试代码。src/test/java目录下的java文件编译到测试classpath目录中    
process-test-classes  
test  使用丹云测试框架运行测试，测试代码不会被打包或部署    
prepare-package  
package  接受编译好的代码，打包成可发布的格式，如jar    
pre-integration-test  
integration-test  
post-integration-test  
verify  
install 将包安装到Maven本地仓库，供本地其他Maven项目使用。    
deploy  将最终的包复制到远程仓库，供其他开发人员和Maven项目使用。    
####  site生命周期  
pre-site  执行一些在生成项目的站点之前需要完成的工作    
site  生成项目站点文档    
post-site 执行一些在生成项目站点之后需要完成的工作    
site-deploy  将生成的项目站点发布到服务器上    


### 镜像    
镜像如果不能使用会导致镜像想要替代的仓库无法访问    
#### Maven中央仓库地址：    
http://repo1.maven.org/maven2/  
#### Maven中央仓库的中国镜像    
http://maven.net.cn/content/groups/public  

