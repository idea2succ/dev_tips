### 组织模块的开发

### 概述
 * 组织模块是一个用户管理自己的人脉，下属，团队，学生，居民等等一个群体
 * 组织类似于群，但又区分与群，有一个区别是用户的发展方式不一样
 
 ### 一些主要的用例
 * 用户通过excel创建属于自己的组织
 * 用户可以管理组织的成员
 * 组织成员的用户可以再分组
 * 受众用户可以自己选择加入或者退出组织，类似于公众号
 
 ### 和其他业务模型的关系
 * 一个用户属于多个组织，一个组织有多个受众用户
 * 一个组织有多个活动，一个活动属于一个组织，或者属于一个地理位置区域
 * 一个组织的分组有一个节点，可以相互沟通
 
 
 ### 普通用户如何加入组织
 * 管理员拉入并且用户开通APP
 * 受众用户申请加入组织
 
### 其他考虑
* 一个组织有一个主页
* 一个组织有一些菜单按钮可以手机交互

### 组织模型 - org
* name
* owner
* description
* zuzhi_type (个人，物业，学校，社区，公司)
* has many user
* has_many small_group 
* has many activity
* has one global node

### 组织模型 - org_user
* id user_id org_id

### 组织模型 org_smallgroup
* id org_id small_group_id

### 用户对组织的取舍
* 可以退出该组织
* 可以退出该用户创建的任何组织
* 可以屏蔽某组织的消息



### 开始原型开发

* 建立一个org模块 padrino g app org
*  padrino g controller base -a org ,建立一个 基础的控制器，用于调试或者集成
*  padrino g model organize name:string description:string owner:integer zuzi_type:string node_id integer -a org
*  rake db:migrate
*  padrino g admin_page organize





   
 
