# Go语言bytes和strings的学习

## Go语言的bytes的使用和strings的使用

```Go
1：
func Index(s, sep []byte) int
使用
bytes.Index([]byte("chicken"), []byte("ken")))
2：
func HasPrefix(s, prefix []byte) bool
使用
bytes.HasSuffix([]byte("Amigo"), []byte("go"))
3：
func Equal(a, b []byte) bool  or   func EqualFold(s,t []byte)bool
使用
bytes.Equal([]byte("Go"),[]byte("Go"))
4:
func Split(s,sep []byte)[][]byte
使用
bytes.Split([]byte("a,b,c"), []byte(","))
5:
func Join(s [][]byte,sep []byte) []byte
使用
s:=[][]byte{[]byte("wo"),[]byte("ai"),[]byte("ni")}
bytes.Join(s,[]byte(","))
6:
func Fields(s []byte) [][]byte //就是按空格进行了分割
 bytes.Fields([]byte("  foo bar  baz   ")
 ["foo" "bar" "baz"]
7:
func NewBuffer(buf []byte) *Buffer
使用
这个函数就是建立一个读写缓冲区。
buff:=make([]byte,20)
databuff:=bytes.NewBuffer(buff)
```

bytes和strings包的方法大致是相同的。
一些在项目中遇见的例子有：

```Go
1：
func TrimSpace(s string) string //（all leading and trailing white space removed。like \t,\n,\r）
使用
strings.TrimSpace(" \t\n Hello, Gophers \n\t\r\n")
Hello, Gophers
2:
func Trim(s string,cutset string)string//(with all leading and trailing Unicode code points contained in cutset removed)
使用
strings.Trim("¡¡¡Hello, Gophers!!!", "!¡")
Hello, Gophers
```