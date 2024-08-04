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

## Computer-system architecture ##
![image](https://github.com/user-attachments/assets/e739666e-d7e3-4538-ab17-ba279d518b4b)
- Desktop system：single processor
- <mark style="color:red;">Parallel system：tightly coupled</mark>
- <mark style="color:red;">Distributed system：loosely coupled</mark>

### Parallel System ###
![image](https://github.com/user-attachments/assets/6381a0b3-02b2-41f3-83ac-3464a261c999)
- <mark style="color:red;">multiprocessor</mark>
- 很多CPU+MEM透過hardware (system bus)連接在一起
    - 透過shared memory
- 目的
    - throughput：增加處理量
    - economical：許多東西共用以節省成本
    - Reliability
- 種類
    - Symmetric multiprocessor system(SMP)
        - 每個CPU都是相同計算功能
    - Asymmetric multiprocessor system
        - 有一個master CPU負責管理，其他slave CPU負責計算

#### 從processor角度 ####
- Multi-Core Processor：在同一個chip上
  ![image](https://github.com/user-attachments/assets/3651861f-7326-4a44-8f81-537bb0b2ed87)
- Many-Core Processor：GPU

#### 從memory角度 ####
- Uniform Memory Access (UMA)
    ![image](https://github.com/user-attachments/assets/849f5921-4479-43b2-bd9e-1b64ef9c0a51)
    - SMP：每一顆CPU都相同
    - Memory access time相同
- Non-Uniform Memory (NUMA)
    ![image](https://github.com/user-attachments/assets/2d7d229a-5680-4c08-affe-036ec9b9fad3)
    - 存取local memory較快
    - 連接remote memory較慢
    - 規模較大，且講究效能
