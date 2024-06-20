#人事管理系统接口文档-V_Last

## 1. 部门管理

### 1.1 部门列表查询

#### 1.1.1 基本信息

> 请求路径：/depts
>
> 请求方式：GET
>
> 接口描述：该接口用于部门列表数据查询



#### 1.1.2 请求参数

无



#### 1.1.3 响应数据

参数格式：application/json

参数说明：

| 参数名         | 类型      | 是否必须 | 备注                             |
| -------------- | --------- | -------- | -------------------------------- |
| code           | number    | 必须     | 响应码，1 代表成功，0 代表失败   |
| msg            | string    | 非必须   | 提示信息                         |
| data           | object[ ] | 非必须   | 返回的数据列表,item 类型: object |
| \|- id         | number    | 非必须   | id                               |
| \|- name       | string    | 非必须   | 部门名称                         |
| \|- createTime | string    | 非必须   | 创建时间                         |
| \|- updateTime | string    | 非必须   | 修改时间                         |

响应数据样例：

```json
{
  "code": 1,
  "msg": "success",
  "data": [
    {
      "id": 1,
      "name": "学工部",
      "createTime": "2022-09-01T23:06:29",
      "updateTime": "2022-09-01T23:06:29"
    },
    {
      "id": 2,
      "name": "教研部",
      "createTime": "2022-09-01T23:06:29",
      "updateTime": "2022-09-01T23:06:29"
    }
  ]
}
```





### 1.2 删除部门

#### 1.2.1 基本信息

> 请求路径：/depts/{id}
>
> 请求方式：DELETE
>
> 接口描述：该接口用于根据ID删除部门数据



#### 1.2.2 请求参数

参数格式：路径参数

参数说明：

| 参数名 | 类型   | 是否必须 | 备注   |
| ------ | ------ | -------- | ------ |
| id     | number | 必须     | 部门ID |

请求参数样例：

```
/depts/1
```



#### 1.2.3 响应数据

参数格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注                           |
| ------ | ------ | -------- | ------------------------------ |
| code   | number | 必须     | 响应码，1 代表成功，0 代表失败 |
| msg    | string | 非必须   | 提示信息                       |
| data   | object | 非必须   | 返回的数据                     |

响应数据样例：

```json
{
    "code":1,
    "msg":"success",
    "data":null
}
```







### 1.3 添加部门

#### 1.3.1 基本信息

> 请求路径：/depts
>
> 请求方式：POST
>
> 接口描述：该接口用于添加部门数据




#### 1.3.2 请求参数

格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注     |
| ------ | ------ | -------- | -------- |
| name   | string | 必须     | 部门名称 |

请求参数样例：

```json
{
	"name": "教研部"
}
```



#### 1.3.3 响应数据

参数格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注                           |
| ------ | ------ | -------- | ------------------------------ |
| code   | number | 必须     | 响应码，1 代表成功，0 代表失败 |
| msg    | string | 非必须   | 提示信息                       |
| data   | object | 非必须   | 返回的数据                     |

响应数据样例：

```json
{
    "code":1,
    "msg":"success",
    "data":null
}
```





### 1.4 根据ID查询

#### 1.4.1 基本信息

> 请求路径：/depts/{id}
>
> 请求方式：GET
>
> 接口描述：该接口用于根据ID查询部门数据




#### 1.4.2 请求参数

参数格式：路径参数

参数说明：

| 参数名 | 类型   | 是否必须 | 备注   |
| ------ | ------ | -------- | ------ |
| id     | number | 必须     | 部门ID |

请求参数样例：

```
/depts/1
```





#### 1.4.3 响应数据

参数格式：application/json

参数说明：

| 参数名         | 类型   | 是否必须 | 备注                           |
| -------------- | ------ | -------- | ------------------------------ |
| code           | number | 必须     | 响应码，1 代表成功，0 代表失败 |
| msg            | string | 非必须   | 提示信息                       |
| data           | object | 非必须   | 返回的数据                     |
| \|- id         | number | 非必须   | id                             |
| \|- name       | string | 非必须   | 部门名称                       |
| \|- createTime | string | 非必须   | 创建时间                       |
| \|- updateTime | string | 非必须   | 修改时间                       |

响应数据样例：

```json
{
  "code": 1,
  "msg": "success",
  "data": {
    "id": 1,
    "name": "学工部",
    "createTime": "2022-09-01T23:06:29",
    "updateTime": "2022-09-01T23:06:29"
  }
}
```





### 1.5 修改部门

#### 1.5.1 基本信息

> 请求路径：/depts
>
> 请求方式：PUT
>
> 接口描述：该接口用于修改部门数据



#### 1.5.2 请求参数

格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注     |
| ------ | ------ | -------- | -------- |
| id     | number | 必须     | 部门ID   |
| name   | string | 必须     | 部门名称 |

请求参数样例：

```json
{
	"id": 1,
	"name": "教研部"
}
```



#### 1.5.3 响应数据

参数格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注                           |
| ------ | ------ | -------- | ------------------------------ |
| code   | number | 必须     | 响应码，1 代表成功，0 代表失败 |
| msg    | string | 非必须   | 提示信息                       |
| data   | object | 非必须   | 返回的数据                     |

响应数据样例：

```json
{
    "code":1,
    "msg":"success",
    "data":null
}
```

















## 2. 员工管理

### 2.1 员工列表查询

#### 2.1.1 基本信息

> 请求路径：/emps
>
> 请求方式：GET
>
> 接口描述：该接口用于员工列表数据的条件分页查询



#### 2.1.2 请求参数

参数格式：queryString

参数说明：

| 参数名称 | 是否必须 | 示例       | 备注                                       |
| -------- | -------- | ---------- | ------------------------------------------ |
| name     | 否       | 张         | 姓名                                       |
| gender   | 否       | 1          | 性别 , 1 男 , 2 女                         |
| begin    | 否       | 2010-01-01 | 范围匹配的开始时间(入职日期)               |
| end      | 否       | 2020-01-01 | 范围匹配的结束时间(入职日期)               |
| page     | 是       | 1          | 分页查询的页码，如果未指定，默认为1        |
| pageSize | 是       | 10         | 分页查询的每页记录数，如果未指定，默认为10 |

请求数据样例：

```shell
/emps?name=张&gender=1&begin=2007-09-01&end=2022-09-01&page=1&pageSize=10
```



#### 2.1.3 响应数据

参数格式：application/json

参数说明：

| 名称           | 类型      | 是否必须 | 默认值 | 备注                                                         | 其他信息          |
| -------------- | --------- | -------- | ------ | ------------------------------------------------------------ | ----------------- |
| code           | number    | 必须     |        | 响应码, 1 成功 , 0 失败                                      |                   |
| msg            | string    | 非必须   |        | 提示信息                                                     |                   |
| data           | object    | 必须     |        | 返回的数据                                                   |                   |
| \|- total      | number    | 必须     |        | 总记录数                                                     |                   |
| \|- rows       | object [] | 必须     |        | 数据列表                                                     | item 类型: object |
| \|- id         | number    | 非必须   |        | id                                                           |                   |
| \|- username   | string    | 非必须   |        | 用户名                                                       |                   |
| \|- name       | string    | 非必须   |        | 姓名                                                         |                   |
| \|- password   | string    | 非必须   |        | 密码                                                         |                   |
| \|- entrydate  | string    | 非必须   |        | 入职日期                                                     |                   |
| \|- gender     | number    | 非必须   |        | 性别 , 1 男 ; 2 女                                           |                   |
| \|- image      | string    | 非必须   |        | 图像                                                         |                   |
| \|- job        | number    | 非必须   |        | 职位, 说明: 1 班主任,2 讲师, 3 学工主管, 4 教研主管, 5 咨询师 |                   |
| \|- deptId     | number    | 非必须   |        | 部门id                                                       |                   |
| \|- createTime | string    | 非必须   |        | 创建时间                                                     |                   |
| \|- updateTime | string    | 非必须   |        | 更新时间                                                     |                   |

响应数据样例：

```json
{
  "code": 1,
  "msg": "success",
  "data": {
    "total": 2,
    "rows": [
       {
        "id": 1,
        "username": "jinyong",
        "password": "123456",
        "name": "金庸",
        "gender": 1,
        "image": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2022-09-02-00-27-53B.jpg",
        "job": 2,
        "entrydate": "2015-01-01",
        "deptId": 2,
        "createTime": "2022-09-01T23:06:30",
        "updateTime": "2022-09-02T00:29:04"
      },
      {
        "id": 2,
        "username": "zhangwuji",
        "password": "123456",
        "name": "张无忌",
        "gender": 1,
        "image": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2022-09-02-00-27-53B.jpg",
        "job": 2,
        "entrydate": "2015-01-01",
        "deptId": 2,
        "createTime": "2022-09-01T23:06:30",
        "updateTime": "2022-09-02T00:29:04"
      }
    ]
  }
}
```







### 2.2 删除员工

#### 2.2.1 基本信息

> 请求路径：/emps/{ids}
>
> 请求方式：DELETE
>
> 接口描述：该接口用于批量删除员工的数据信息



#### 2.2.2 请求参数

参数格式：路径参数

参数说明：

| 参数名 | 类型       | 示例  | 是否必须 | 备注         |
| ------ | ---------- | ----- | -------- | ------------ |
| ids    | 数组 array | 1,2,3 | 必须     | 员工的id数组 |

请求参数样例：

```
/emps/1,2,3
```



#### 2.2.3 响应数据

参数格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注                           |
| ------ | ------ | -------- | ------------------------------ |
| code   | number | 必须     | 响应码，1 代表成功，0 代表失败 |
| msg    | string | 非必须   | 提示信息                       |
| data   | object | 非必须   | 返回的数据                     |

响应数据样例：

```json
{
    "code":1,
    "msg":"success",
    "data":null
}
```







### 2.3 添加员工

#### 2.3.1 基本信息

> 请求路径：/emps
>
> 请求方式：POST
>
> 接口描述：该接口用于添加员工的信息



#### 2.3.2 请求参数

参数格式：application/json

参数说明：

| 名称      | 类型   | 是否必须 | 备注                                                         |
| --------- | ------ | -------- | ------------------------------------------------------------ |
| username  | string | 必须     | 用户名                                                       |
| name      | string | 必须     | 姓名                                                         |
| gender    | number | 必须     | 性别, 说明: 1 男, 2 女                                       |
| image     | string | 非必须   | 图像                                                         |
| deptId    | number | 非必须   | 部门id                                                       |
| entrydate | string | 非必须   | 入职日期                                                     |
| job       | number | 非必须   | 职位, 说明: 1 班主任,2 讲师, 3 学工主管, 4 教研主管, 5 咨询师 |

请求数据样例：

```json
{
  "image": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2022-09-03-07-37-38222.jpg",
  "username": "linpingzhi",
  "name": "林平之",
  "gender": 1,
  "job": 1,
  "entrydate": "2022-09-18",
  "deptId": 1
}
```





#### 2.3.3 响应数据

参数格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注                           |
| ------ | ------ | -------- | ------------------------------ |
| code   | number | 必须     | 响应码，1 代表成功，0 代表失败 |
| msg    | string | 非必须   | 提示信息                       |
| data   | object | 非必须   | 返回的数据                     |

响应数据样例：

```json
{
    "code":1,
    "msg":"success",
    "data":null
}
```





### 2.4 根据ID查询

#### 2.4.1 基本信息

> 请求路径：/emps/{id}
>
> 请求方式：GET
>
> 接口描述：该接口用于根据主键ID查询员工的信息



#### 2.4.2 请求参数

参数格式：路径参数

参数说明：

| 参数名 | 类型   | 是否必须 | 备注   |
| ------ | ------ | -------- | ------ |
| id     | number | 必须     | 部门ID |

请求参数样例：

```
/emps/1
```



#### 2.4.3 响应数据

参数格式：application/json

参数说明：

| 名称           | 类型   | 是否必须 | 默认值 | 备注                                                         | 其他信息 |
| -------------- | ------ | -------- | ------ | ------------------------------------------------------------ | -------- |
| code           | number | 必须     |        | 响应码, 1 成功 , 0 失败                                      |          |
| msg            | string | 非必须   |        | 提示信息                                                     |          |
| data           | object | 必须     |        | 返回的数据                                                   |          |
| \|- id         | number | 非必须   |        | id                                                           |          |
| \|- username   | string | 非必须   |        | 用户名                                                       |          |
| \|- name       | string | 非必须   |        | 姓名                                                         |          |
| \|- password   | string | 非必须   |        | 密码                                                         |          |
| \|- entrydate  | string | 非必须   |        | 入职日期                                                     |          |
| \|- gender     | number | 非必须   |        | 性别 , 1 男 ; 2 女                                           |          |
| \|- image      | string | 非必须   |        | 图像                                                         |          |
| \|- job        | number | 非必须   |        | 职位, 说明: 1 班主任,2 讲师, 3 学工主管, 4 教研主管, 5 咨询师 |          |
| \|- deptId     | number | 非必须   |        | 部门id                                                       |          |
| \|- createTime | string | 非必须   |        | 创建时间                                                     |          |
| \|- updateTime | string | 非必须   |        | 更新时间                                                     |          |

响应数据样例：

```json
{
  "code": 1,
  "msg": "success",
  "data": {
    "id": 2,
    "username": "zhangwuji",
    "password": "123456",
    "name": "张无忌",
    "gender": 1,
    "image": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2022-09-02-00-27-53B.jpg",
    "job": 2,
    "entrydate": "2015-01-01",
    "deptId": 2,
    "createTime": "2022-09-01T23:06:30",
    "updateTime": "2022-09-02T00:29:04"
  }
}
```







### 2.5 修改员工
#### 2.5.1 基本信息

> 请求路径：/emps
>
> 请求方式：PUT
>
> 接口描述：该接口用于修改员工的数据信息



#### 2.5.2 请求参数

参数格式：application/json

参数说明：

| 名称      | 类型   | 是否必须 | 备注                                                         |
| --------- | ------ | -------- | ------------------------------------------------------------ |
| id        | number | 必须     | id                                                           |
| username  | string | 必须     | 用户名                                                       |
| name      | string | 必须     | 姓名                                                         |
| gender    | number | 必须     | 性别, 说明: 1 男, 2 女                                       |
| image     | string | 非必须   | 图像                                                         |
| deptId    | number | 非必须   | 部门id                                                       |
| entrydate | string | 非必须   | 入职日期                                                     |
| job       | number | 非必须   | 职位, 说明: 1 班主任,2 讲师, 3 学工主管, 4 教研主管, 5 咨询师 |

请求数据样例：

```json
{
  "id": 1,
  "image": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2022-09-03-07-37-38222.jpg",
  "username": "linpingzhi",
  "name": "林平之",
  "gender": 1,
  "job": 1,
  "entrydate": "2022-09-18",
  "deptId": 1
}
```



#### 2.5.3 响应数据

参数格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注                           |
| ------ | ------ | -------- | ------------------------------ |
| code   | number | 必须     | 响应码，1 代表成功，0 代表失败 |
| msg    | string | 非必须   | 提示信息                       |
| data   | object | 非必须   | 返回的数据                     |

响应数据样例：

```json
{
    "code":1,
    "msg":"success",
    "data":null
}
```







### 2.6 文件上传

#### 2.6.1 基本信息

> 请求路径：/upload
>
> 请求方式：POST
>
> 接口描述：上传图片接口



#### 2.6.2 请求参数

参数格式：multipart/form-data

参数说明：

| 参数名称 | 参数类型 | 是否必须 | 示例 | 备注 |
| -------- | -------- | -------- | ---- | ---- |
| image    | file     | 是       |      |      |



#### 2.6.3 响应数据

参数格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注                           |
| ------ | ------ | -------- | ------------------------------ |
| code   | number | 必须     | 响应码，1 代表成功，0 代表失败 |
| msg    | string | 非必须   | 提示信息                       |
| data   | object | 非必须   | 返回的数据，上传图片的访问路径 |

响应数据样例：

```json
{
    "code": 1,
    "msg": "success",
    "data": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2022-09-02-00-27-0400.jpg"
}
```





## 3. 登录接口

### 3.1 登录

#### 3.1.1 基本信息

> 请求路径：/login   和 /user/login  
>
> 请求方式：POST
>
> 接口描述：该接口用于用户登录人事管理系统系统，登录完毕后，系统下发JWT令牌。 



#### 3.1.2 请求参数

参数格式：application/json

参数说明：

| 名称     | 类型   | 是否必须 | 备注   |
| -------- | ------ | -------- | ------ |
| username | string | 必须     | 用户名 |
| password | string | 必须     | 密码   |

请求数据样例：

```json
{
	"username": "jinyong",
    "password": "123456"
}
```



#### 3.1.3 响应数据

参数格式：application/json

参数说明：

| 名称 | 类型   | 是否必须 | 默认值 | 备注                     | 其他信息 |
| ---- | ------ | -------- | ------ | ------------------------ | -------- |
| code | number | 必须     |        | 响应码, 1 成功 ; 0  失败 |          |
| msg  | string | 非必须   |        | 提示信息                 |          |
| data | string | 必须     |        | 返回的数据 , jwt令牌     |          |



响应数据样例：

```json
{
  "code": 1,
  "msg": "success",
  "data": "eyJhbGciOiJIUzI1NiJ9.eyJuYW1lIjoi6YeR5bq4IiwiaWQiOjEsInVzZXJuYW1lIjoiamlueW9uZyIsImV4cCI6MTY2MjIwNzA0OH0.KkUc_CXJZJ8Dd063eImx4H9Ojfrr6XMJ-yVzaWCVZCo"
}
```





#### 3.1.4 备注说明

> 用户登录成功后，系统会自动下发JWT令牌，然后在后续的每次请求中，都需要在请求头header中携带到服务端，请求头的名称为 token ，值为 登录时下发的JWT令牌。
>
> 如果检测到用户未登录，则会返回如下固定错误信息：
>
> ```json
> {
> 	"code": 0,
> 	"msg": "NOT_LOGIN",
> 	"data": null
> }
> ```



## 4 .薪资管理

**在薪资管理中不设置删除和新增的**

**在员工添加的时候就同步添加一个员工的工资条（只有基础的工资，根据职位定一个基础的工资，其余为0）**

### 4.1薪资查询：

> 请求路径：/salary
>
> 请求方式：GET
>
> 接口描述：该接口用于薪资列表数据的条件分页查询



#### 4.1.2 请求参数

参数格式：queryString

参数说明：

| 参数名称    | 是否必须 | 示例    | 备注                                       |
| ----------- | -------- | ------- | ------------------------------------------ |
| name        | 否       | 张      | 姓名                                       |
| gender      | 否       | 1       | 性别 , 1 男 , 2 女                         |
| totalSalary | 否       | 10000.0 | 指定薪资的查询                             |
| page        | 是       | 1       | 分页查询的页码，如果未指定，默认为1        |
| pageSize    | 是       | 10      | 分页查询的每页记录数，如果未指定，默认为10 |

请求数据样例：

```shell
/salary?name=张&gender=1&totalSalary=20000&page=1&pageSize=10
```



#### 4.1.3 响应数据

参数格式：application/json

参数说明：



| 名称            | 类型      | 是否必须 | 默认值 | 备注                    | 其他信息           |
| --------------- | --------- | -------- | ------ | ----------------------- | ------------------ |
| code            | number    | 必须     |        | 响应码, 1 成功 , 0 失败 |                    |
| msg             | string    | 非必须   |        | 提示信息                |                    |
| data            | object    | 必须     |        | 返回的数据              |                    |
| \|- total       | number    | 必须     |        | 总记录数                |                    |
| \|- rows        | object [] | 必须     |        | 数据列表                | item 类型: object  |
| \|- id          | number    | 非必须   |        | id                      | 不显示             |
| \|- name        | string    | 非必须   |        | 姓名                    | 在员工信息表中查询 |
| \|- password    | string    | 非必须   |        | 密码                    | 不显示             |
| \|- image       | string    | 非必须   |        | 图像                    |                    |
| \|- job         | number    | 非必须   |        | 职位, 说明:             |                    |
| \|- deptId      | number    | 非必须   |        | 部门id                  | 部门中必须含有     |
| \|- basicSalary | number    | 非必须   |        | 基础工资                |                    |
| \|-meritSalary  | number    | 非必须   |        | 绩效工资                |                    |
| \|-bonusSalary  | number    | 非必须   |        | 奖金                    |                    |
| \|-subsidSalary | number    | 非必须   |        | 补贴                    |                    |
| \|- createTime  | string    | 非必须   |        | 创建时间                |                    |
| \|- updateTime  | string    | 非必须   |        | 更新时间                |                    |

### 4.2薪资修改

#### 4.2.1 基本信息

> 请求路径：/salary
>
> 请求方式：PUT
>
> 接口描述：该接口用于修改薪资数据



#### 4.2.2 请求参数

格式：application/json

参数说明：

| 参数名            | 类型   | 是否必须 | 备注         |
| ----------------- | ------ | -------- | ------------ |
| empId             | number | 必须     | 员工的薪资ID |
| \|- basicSalary   | number | 非必须   | 基础薪资     |
| \|- meritSalary   | number | 非必须   | 绩效         |
| \|- bonusSalary   | number | 非必须   | 奖金         |
| \|- subsidySalary | number | 非必须   | 津贴（补助） |



请求参数样例：

```json
{
	"id": 1,
	"basicSalary":10000,
    "meritSalary":1000,
    "bonusSalary":500,
    "subsidySalary":200
}
```



#### 4.2.3 响应数据

参数格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注                           |
| ------ | ------ | -------- | ------------------------------ |
| code   | number | 必须     | 响应码，1 代表成功，0 代表失败 |
| msg    | string | 非必须   | 提示信息                       |
| data   | object | 非必须   | 返回的数据                     |

响应数据样例：

```json
{
    "code":1,
    "msg":"success",
    "data":null
}
```

  

##  5.数据统计

### 5.1 员工统计 ：

#### 5.1.1员工性别（饼状图）

> 请求路径：/emp-report/gender
>
> 请求方式：GET
>
> 接口描述：该接口用于员工性别数量的统计

#####  请求参数

参数格式：queryString

参数说明：无参数

#####  响应参数

参数格式：application/json

参数说明：

| 名称       | 类型   | 是否必须 | 默认值 | 备注                    | 其他信息 |
| ---------- | ------ | -------- | ------ | ----------------------- | -------- |
| code       | number | 必须     |        | 响应码, 1 成功 , 0 失败 |          |
| msg        | string | 非必须   |        | 提示信息                |          |
| data       | object | 必须     |        | 返回的数据              |          |
| \|- female | number | 必须     |        | 女性员工总人数          |          |
| \|- male   | number | 必须     |        | 男性员工总人数          |          |

响应数据样例：

```json
{
  "code": 1,
  "msg": "success",
  "data": {
    "female": 50,
    "male": 60
  }
}
```



#### 5.1.2部门员工统计 （柱状图）

> 请求路径：/emp-report/deptNumber
>
> 请求方式：GET
>
> 接口描述：该接口用于部门员工数量的统计

#####  请求参数

参数格式：queryString

参数说明：无参数

##### 响应参数

参数格式：application/json

参数说明：

| 参数名            | 类型      | 是否必须 | 备注                             |
| ----------------- | --------- | -------- | -------------------------------- |
| code              | number    | 必须     | 响应码，1 代表成功，0 代表失败   |
| msg               | string    | 非必须   | 提示信息                         |
| data              | object[ ] | 非必须   | 返回的数据列表,item 类型: object |
| \|- name          | string    | 非必须   | 部门名称                         |
| \|- employeeCount | number    | 非必须   | 部门员工人数                     |

响应数据样例：

```json
{
  "code": 1,
  "msg": "success",
  "data": [
    {
      "name": "研发部",
      "employeeCount": 20
    },
  	{
      "name": "销售部部",
      "employeeCount": 30
    }
  ]
}
```

### 5.2 薪资统计分析

#### 5.2.1 部门平均薪资（柱状图）

> 请求路径：/salary-report/deptSalary
>
> 请求方式：GET
>
> 接口描述：该接口用于部门员工数量的统计

##### 请求参数

参数格式：queryString

参数说明：无参数

##### 响应参数

参数格式：application/json

参数说明：

| 参数名            | 类型      | 是否必须 | 备注                             |
| ----------------- | --------- | -------- | -------------------------------- |
| code              | number    | 必须     | 响应码，1 代表成功，0 代表失败   |
| msg               | string    | 非必须   | 提示信息                         |
| data              | object[ ] | 非必须   | 返回的数据列表,item 类型: object |
| \|- name          | string    | 非必须   | 部门名称                         |
| \|- averageSalary | number    | 非必须   | 部门平均薪资                     |

响应数据样例：

```json
{
  "code": 1,
  "msg": "success",
  "data": [
    {
      "name": "研发部",
      "employeeCount": 20
    },
  	{
      "name": "销售部部",
      "employeeCount": 30
    }
  ]
}
```



#### 5.2.2薪资分布（箱线图）

> 请求路径：/salary-report/averageSalary
>
> 请求方式：GET
>
> 接口描述：该接口用于薪资分布的统计计算

##### 请求参数

参数格式：queryString

参数说明：无参数

##### 响应参数

参数格式：application/json

参数说明：

| 参数名      | 类型   | 是否必须 | 备注                             |
| ----------- | ------ | -------- | -------------------------------- |
| code        | number | 必须     | 响应码，1 代表成功，0 代表失败   |
| msg         | string | 非必须   | 提示信息                         |
| data        | object | 非必须   | 返回的数据列表,item 类型: object |
| \|- minimum |        | 非必须   | 最小值                           |
| \|-Q1       | number | 非必须   | 下四分点                         |
| \|-median   | number | 非必须   | 中位数                           |
| \|-Q3       | number | 非必须   | 上四分点                         |
| \|-maximum  | number | 非必须   | 最大值                           |

响应数据样例：

```json
{
  "code": 1,
  "msg": "success",
  "data": 
    {
      "minimum": 1000,
      "Q1": 3000,
      "median": 5000,
      "Q3": 7000,
      "maximum": 10000
    }
  
}
```



## 6.修改用户信息

### 6.1 修改用户信息

#### 6.1.1 基本信息

> 请求路径：/update
>
> 请求方式：Post
>
> 接口描述：该接口用于修改用户名和用户密码



#### 6.1.2 请求参数

格式：application/json

参数说明：

| 参数名   | 类型   | 是否必须 | 备注       |
| -------- | ------ | -------- | ---------- |
| id       | number | 必须     | 用户ID     |
| username | string | 非必须   | 用户名     |
|          |        | 非必须   | 用户新密码 |

请求参数样例：

```json
{
	"id": 1,
	"name": "admin",
    "password": "123456“
}
```



#### 6.1.3 响应数

参数格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注                           |
| ------ | ------ | -------- | ------------------------------ |
| code   | number | 必须     | 响应码，1 代表成功，0 代表失败 |
| msg    | string | 非必须   | 提示信息                       |
| data   | object | 非必须   | 返回的数据                     |

响应数据样例：

```json
{
    "code":1,
    "msg":"success",
    "data":null
}
```



### 6.12修改用户信息

#### 6.2.1 基本信息

> 请求路径：/reset-password
>
> 请求方式：Post
>
> 接口描述：该接口用于用户忘记密码重置密码



#### 6.2.2 请求参数

格式：application/json

参数说明：

| 参数名   | 类型   | 是否必须 | 备注         |
| -------- | ------ | -------- | ------------ |
| name     | string | 必须     | 用户真实姓名 |
| username | string | 必须     | 用户名       |
| password | string | 必须     | 用户新密码   |

请求参数样例：

```json
{
	"name": "欣喜喜",
	"username": "admin",
    "password": "123456“
}
```



#### 6.2.3 响应参数

参数格式：application/json

参数说明：

| 参数名 | 类型   | 是否必须 | 备注                           |
| ------ | ------ | -------- | ------------------------------ |
| code   | number | 必须     | 响应码，1 代表成功，0 代表失败 |
| msg    | string | 非必须   | 提示信息                       |
| data   | object | 非必须   | 返回的数据                     |

响应数据样例：

```json
{
    "code":1,
    "msg":"success",
    "data":null
}
```

