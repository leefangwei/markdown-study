# Flow chat 流程图

## 说明

### 代码详解

形参|实参|含义
:-:|:-:|:-:
tag|st|标签（可以自定义）
=>|=>|赋值
type|start|类型（6种[类型](#type)）
content|开始|描述内容（可以自定义）

### type {#type}

类型|含义
:-:|:-:
start|启动
end|结束
operation|程序
subroutine|子程序
condition|条件
inputoutput|输入、输出

---

```flow
st=>start: 开始
e=>end: 结束
op=>subroutine: 我的操作
op1=>operation: 我的操作1
cond=>condition: 判断确认？
  
st->op->op1->cond
cond(yes)->e
cond(no)->op
```

---

```flow
st=>start: 鉴权
e=>end: 结束退出
cond1=>condition: user==bgbiao
product=ddaotian
productcheck=>condition: ddaotian类型产品库存
(ecs,bss,vpc,eip,hids)
  
  
op1=>operation: 发起预订请求
拆单并库存检测
  
op2=>operation: info:生产指定类型产品
(DAOTIAN:ecs,natip,eip,hids)
op3=>operation: 鉴权失败
op4=>operation: 库存检测失败
  
io1=>inputoutput: 返回产品相关信息
ECS,NATIP,EIP,HIDS
  
io2=>inputoutput: info:无此类型产品
  
  
  
st->cond1
cond1(yes)->op1->productcheck(yes)->op2->io1->e
cond1(no)->op3->e
cond1(yes)->op1->productcheck(no)->op4->io2->e
```
