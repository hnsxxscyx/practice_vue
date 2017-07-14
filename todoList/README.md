### 介绍
本项目为复现[TodoMVC](https://cn.vuejs.org/v2/examples/todomvc.html)所做的练手项目
### 项目分析
- 样式
字体、删除线和颜色需要特别注意
- 功能
    - item的添加、选择完成、全选
    - item本身的状态筛选
### 个人所想功能实现
- 结构
    - 标题
    - 输入框
    - 列表
        - 具体项需要添加checkbox以表示项目完成
    - 显示切换按钮
- 数据实现
    - 本地存储——还没想好
- Vue特性
    - 使用模版绑定DOM与数据
    - 使用表单控件绑定绑定文本数据、布尔值
### 遇到的难点
- All、Active、Completed的切换
    - 最初构想：修改visible的值为true(all)、item.completed属性的值或非值，但在方法中获取不到item值，也无法一一对应的设置li的属性
    - 完成构想：v-show属性值是表达式且可访问到item.completed，则使用三元选择符判断visible值，且v-for优先级比if更高