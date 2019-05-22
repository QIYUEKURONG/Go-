# Go语言的序列化和反序列化

## Go语言使用json

1：包名为"encoding/json"
例子：
我们使用go语言的结构体来看一看

```Go
import (
    "fmt"
    "encoding/json"
    "os"
)
type mess struct{
    Name string
    Age  int
}
func JsonShun(data *mess)[]byte{
    buf,err:=json.Marshal(mess)
    if err!=nil{
        fmt.Println("json marshal error")
        os.Exit(-1)
        }
    return buf
}
func JsonFan(result []byte)mess{
    var mes mess
    err:=json.Unmarshal(result，&mes)
    if err!=nil{
        fmt.Println("JsonFan find error.sorry")
    }
    return mes
}
func main(){
    data :=mess{"WENJIE",20}
    result:=JsonShun(&data)
    fmt.Println(result)
    mes:=JsonFan(result)
    fmt.Println(mes)
}
```
2:Go语言json的标签的使用

```Gos
type Product struct {
    Name      string  `json:"name"`
    ProductID int64   `json:"-"` // 表示不进行序列化
    Number    int     `json:"number"`
    Price     float64 `json:"price"`
    IsOnSale  bool    `json:"is_on_sale,string"`
}
// 序列化过后，可以看见
{"name":"Xiao mi 6","number":10000,"price":2499,"is_on_sale":"false"}
```
