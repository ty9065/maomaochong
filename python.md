## sublime Text2 快捷键：  
快捷键|含义
---------| ---------
command + B  |  运行
command + `  |  控制台

---

## python笔记
字符串方法 	|  含义	
---------| ---------
title()  |  字符串每个单词首字母大写 
strip()  |  删除字符串开头和结尾的空白

## 目录
* [函数](#函数)
    * [传递任意数量的实参](#传递任意数量的实参)
    * [使用任意数量的关键字实参](#使用任意数量的关键字实参)
    * [模块导入](#模块导入)

### 函数
#### 传递任意数量的实参
```py
#----形参名*toppings中的星号让python创建一个名为toppings的空元组，并将收到的所有值都封装到这个元组中----

def make_pizza(*toppings):
    print toppings

make_pizza('pepperoni')
make_pizza('mushrooms','green peppers','extra cheese')
```
输出：
```py
('pepperoni',)
('mushrooms', 'green peppers', 'extra cheese')
```

**注意**：若函数接受不同类型的实参，则*toppings应放在最后（与形参默认值类似）。

-----

#### 使用任意数量的关键字实参
```py
#--形参**user_info中的两个星号让python创建一个名为user_info的空字典，并将收到的所有名称——值对都封装到这个字典中--

def build_profile(first, last, **user_info):
    profile = {}
    profile['first_name'] = first
    profile['last_name'] = last
    for key, value in user_info.items():
        profile[key] = value
    return profile

user_profile = build_profile('albert', 'einstein', location='princeton', field='physics')
print user_profile
```
输出：
`{'field': 'physics', 'first_name': 'albert', 'last_name': 'einstein', 'location': 'princeton'}`

------

#### 模块导入
模块 是扩展名为.py的文件

```py
#module_name.py
def function_0():
    pass

def function_1():
    pass

def function_2():
    pass
···
```

##### 导入整个模块：
- `import module_name`  
调用函数使用句点：`module_name.function_name()`

给模块指定别名：`import module_name as mn`

##### 导入特定的函数：（这个语法调用函数时无需使用句点）
- 导入模块的一个函数：`from module_name import function_name`
- 导入模块的多个函数：`from module_name import function_0, function_1, function_2`
- 导入模块的所有函数：`from module_name import *`（不推荐，函数名可能重复）

给函数指定别名：`from module_name import function_name as fn`  
*别名好处：导入的函数的名称可能与程序中现有的名称冲突，或者函数的名称太长*

------

