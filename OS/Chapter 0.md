# Chapter 0 #

## Mainframe Systems：專門處理某件事的機器 ##
<mark style="color:red;"> Batch → Multi-programming → Time-shared </mark>
### Batch ###
- 一次處理一個job
- user和jobs沒有interaction
  - time-sharing解決沒有interaction的問題
- CPU一直idle
  - 因為I/O速度 <<< CPU速度
  - multi-programming解決此問題

### Multi-programming ###
- 載入多個job，提高CPU使用率
- Spooling (Simultaneous Peripheral Operation On-Line)
  - 當I/O完成時通知CPU
- 目的：增加資源使用率
![image](https://github.com/user-attachments/assets/c1433c37-66a4-4f6d-9fef-b150f2a7a5e8)

### Time-sharing (Multi-tasking) ###
- 目的：
  - 實現interactive (透過鍵盤、螢幕)
  - 很短的response time
- 許多使用者可以同時輸入(simultaneously)
  - 許多時候都在等待使用者輸入
  - 每個程式執行millisecond後換其他程式
- 把CPU的執行變成許多個time slot，所有在系統裡的程式輪流使用time slot
  - 每個使用者執行millisecond
- Virtual memory / synchornization / deadlock
