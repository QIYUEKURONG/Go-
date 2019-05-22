# Go语言提供的流程控制语言包括

if，switch，for，goto，select(用于监听channel(通道))

## if表达式

```GO
if a == 100 {
       /* if 条件语句为 true 执行 */
       if b == 200 {
          /* if 条件语句为 true 执行 */
          fmt.Printf("a 的值为 100 ， b 的值为 200\n" );
       }
   }
```

## for循环表达式

```Go
//无限循环
for{
    block
}
// while循环，在Go语言中没有while关键字
for boolExpression{

}(注意到这个boolExpression是没有括号的)
// 迭代字符串
for index, char := range aString{ 
}
```

## 跳转语句(goto)

```Go
goto(设置一个标签，然后跳转到此标签出)
```

## switch语句

```Go
// 没有表达式，默认为True值，匹配分支中值为True的分支
switch{
     case value < minimum:
        return minimum
    case value > maximum:
        return maximum
    default:
        return value
}
//当然switch后面是可以有值的
```
