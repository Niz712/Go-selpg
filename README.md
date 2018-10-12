# Go-selpg
CLI 命令行实用程序开发基础-selpg



- Install

  ```
  go get github.com/Niz712/Go-selpg
  ```



- Usage

![usage](/images/usage.png)



## 测试

1. `$ selpg -s1 -e1 input_file`

   该命令将把“input_file”的第 1 页写至标准输出（也就是屏幕），因为这里没有重定向或管道。

   ![1](/images/1.png)

2. `$ selpg -s1 -e1 < input_file`

   该命令与示例 1 所做的工作相同，但在本例中，selpg 读取标准输入，而标准输入已被 shell／内核重定向为来自“input_file”而不是显式命名的文件名参数。输入的第 1 页被写至屏幕。

   ![2](/images/2.png)

3. `other_command | selpg -s10 -e20`

   “other_command”的标准输出被 shell／内核重定向至 selpg 的标准输入。将第 10 页到第 20 页写至 selpg 的标准输出（屏幕）。

   ![3](/images/3.png)

4. `$ selpg -s10 -e20 input_file >output_file`

   selpg 将第 10 页到第 20 页写至标准输出；标准输出被 shell／内核重定向至“output_file”。

   ![4](/images/4.png)