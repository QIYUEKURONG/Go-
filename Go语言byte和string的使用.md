# Go语言bytes和string的学习

## Go语言的bytes的使用

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
func NewBuffer(buf []byte) *Buffer


```

