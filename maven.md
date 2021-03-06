# maven 
## 1.Maven两大核心
  - ### 依赖管理:就是对jar包进行管理
![](/images/Maven/maven1.png)
  - ### 项目构建:项目在编码完成后,对项目进行编译,测试,打包,部署等一系列的操作都通过命令来实现
  ## 2. 通过Maven命令将web项目发布至tomcat
  ![](/images/Maven/maven2.png)
  ## 3. Maven目录结构说明
  ![](/images/Maven/maven3.png)
  ## 4. Maven环境变量配置
  ## 5. 查看Maven版本信息
  ![](/images/Maven/maven4.png)
  ## 6. Maven仓库类型
  ![](/images/Maven/maven5.png)
  - ### 配置本地仓库
    - ### 找到jar仓库压缩包
    - ### 解压到本地磁盘
    - ### 配置本地仓库:让maven程序知道仓库在哪里
      ![](/images/Maven/maven6.png)
  ## 7. Maven项目标准目录结构
  ![](/images/Maven/maven7.png)
  ## 8. Maven常用命令
  - ### clear 清理:将项目跟目录下的target目录清理掉
  - ### compile 编译:将项目中的.java文件编译为.class文件
  - ### test 单元测试:将项目跟目录下src/test/java目录下的单元测试类都会执行(单元测试类名要求:xxxTest.java)
  - ### package 打包:将项目打包,打包项目根目录下target目录
    - ### web project --- war包
    - ### java project --- jar包
  - ### install 安装:解决本地多个项目公用一个jar包,打包到本地仓库
  ## 9. Maven项目的生命周期
  - ### 在Maven中存在"三套"生命周期,每一套生命周期相互独立,互不影响.在一套生命周期内,执行后面的命令前面操作会自动执行
    - ### cleanLifeCycle : 清理生命周期 claar 
    - ### defaultLifeCycle : 默认生命周期 (compile,test,package,install,deploy) 
  ## 10. Maven聚合与继承
  - #### 聚合是用于快速构建项目，是表示项目与项目之间的关系。
    - #### 对于聚合模块来说，它知道哪些被聚合的模块(通过modules元素)，但那些被聚合的模块不知道这个聚合模块的存在。
  - #### 继承是为了消除重复的配置。
    - #### 对于继承关系的父POM来说，它不知道哪些子模块继承于它，但那些子模块都必须知道自己的父POM是什么。
    - #### 像 dependencies 这样可以被子类继承的元素还有下面几个元素： 
      - #### groupId
      - #### version
      - #### description
      - #### organization
      - #### inceptionYear
      - #### url
      - #### developers
      - #### contributors
      - #### distributionManagement
      - #### issueManagement
      - #### ciManagement
      - #### scm
      - #### mailingLists
      - #### properties
      - #### dependencies
      - #### dependencyManagement
      - #### repositories
      - #### build
      - #### reporting
