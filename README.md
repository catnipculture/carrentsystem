> #### 作者主页：[舒克日记](https://blog.csdn.net/cativen)
>
>  简介：Java领域优质创作者、Java项目、学习资料、技术互助
>
> <b><font color=red>文中获取源码</font></b>

# 项目介绍

汽车租赁系统后端采用了spring，spring mvc，mybatis框架，前端使用了layui，界面美观。

包含功能：客户管理，车辆管理，出租，出租单管理，汽车入库，检查单管理，菜单管理，用户管理，角色管理，日志管理，统计分析等。

该毕业设计功能涵盖了大部分汽车租赁中的业务需求，特点是业务功能较多，有助于学生加深业务到技术的理解。


# 环境要求

1.运行环境：最好是java jdk1.8,我们在这个平台上运行的。其他版本理论上也可以。 

2.IDE环境：IDEA,Eclipse,Myeclipse都可以。推荐IDEA; 

3.tomcat环境：Tomcat7.x,8.X,9.x版本均可 

4.硬件环境：windows7/8/10 4G内存以上；或者Mac OS; 

5.是否Maven项目：是；查看源码目录中是否包含pom.xml;若包含，则为maven项目，否则为非maven.项目 

6.数据库：MySql5.7/8.0等版本均可；



# 技术栈

运行环境：jdk8 + tomcat9 + mysql5.7 + windows10

服务端技术：Java、Spring、SpringMVC、Mybatis，SSM



# 使用说明

1.使用Navicati或者其它工具，在mysql中创建对应sq文件名称的数据库，并导入项目的sql文件； 

2.使用IDEA/Eclipse/MyEclipse导入项目，修改配置，运行项目； 

3.将项目中config-propertiesi配置文件中的数据库配置改为自己的配置，然后运行；

# 运行指导

idea导入源码空间站顶目教程说明(Vindows版)-ssm篇：

http://mtw.so/5MHvZq 

源码地址：[http://www.codegym.top](http://www.codegym.top/)




# 运行截图

#### **数据库设计**

![image-20241022000822978](https://img-blog.csdnimg.cn/img_convert/2d56e154305362031c9d4d42a9d4f8fd.png)



![image-20241022000842415](https://img-blog.csdnimg.cn/img_convert/d9dba98e90b4d6c9b800f194e5e77911.png)

![image-20241022000857628](https://img-blog.csdnimg.cn/img_convert/77904c7c677304d075833482bb677d5c.png)

![image-20241022000912031](https://img-blog.csdnimg.cn/img_convert/2828e6ca5e88f9f10b36c37aac39a0e2.png)

![image-20241022000925068](https://img-blog.csdnimg.cn/img_convert/bf2be11f543191caca557e02f0fcadb1.png)

![image-20241022000936495](https://img-blog.csdnimg.cn/img_convert/d861c00df5cd4b053103a9cc423315b2.png)

![image-20241022000949288](https://img-blog.csdnimg.cn/img_convert/fec16aa6c5dc1252109874ddd3317b1b.png)

![image-20241022001006536](https://img-blog.csdnimg.cn/img_convert/ef0f59b0406da35d413f5a4954a73057.png)

### 代码

```java
public interface IDetailStoreGoodsService extends IService<DetailStoreGoods> {


    void saveIn(DetailStoreGoods detailStoreGoods, String token);

    Page<DetailStoreGoodsVo> queryPageByQoIn(QueryDetailStoreGoods qo);

    void delIn(String cn);

    Page<DetailStoreGoodsOutVo> queryPageByQoOut(QueryDetailStoreGoodsOut qo);

    Map<String ,Object> initOutOptions();

    List<Map<String,Object>> changeOutGoods(Long gid);

    List<Map<String,Object>> changeOutStore(Long storeId);

    DetailStoreGoodsOutVo queryOutGoods(Long goodsId, Long storeId);

    void saveOut(DetailStoreGoods detailStoreGoods, String token);
}
```




