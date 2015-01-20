# go-timer-wheel

����ʱ���ֵ�����ʱ���ȿ�
![wheel L](docs/wheel.png "wheel")

=========================
��װ��ʽ
```go
package main


import (
        "fmt"
        github.com/zhangwei1234/go-timer-wheel/timerWheel"
)

func main() {
    wheel := timerWheel.NewTimerWheel()//��ʼ��
	wheel.Start()//����
	wheel.AddTask(&MyTask{}, 4 * time.Second)
}

type MyTask struct {
	
}

func(tk *MyTask) Expire() {
	fmt.Printf("-----------------> ִ�� \n")	
}

```

## Developing

You can run the tests with:

go get -d ./...
go test ./...