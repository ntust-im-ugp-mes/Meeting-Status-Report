# 第一週預定進度（190114）

### **[硬體部分]**
* **機台模擬：**
  * 以樹莓派充當機台
  * 並能利用感測器（如紅外線）感知物品進出狀況，傳回給MES系統
  * 能接受來自MES的命令並動作（如開始加工、中斷等）
* **倉儲部分：**
  * 以樹莓派充當一簡易倉庫，裡面只需要放一種物品
  * 感測器能感測物品進出狀況，並回報給MES
* **品管檢測部分：**
  * 以其中一個樹莓派充當品質檢測機器，物品加工後最後會通過本檢測機台
  * 能回報物品進出狀況（同一般機台）及檢測規格（如10.02公分，以常態分布亂數給定）給MES
  </br>
    
### **[MES系統部分]**
* **生產監控部分：**
  * 物件追蹤（物品在哪裡）與機台追蹤（機器在做啥）功能實作
* **作業排程部分：**
  * 不可佔用且視整個系統為單一單元的先進先出（FIFO）排程功能實作
  * 能顯示目前的排程甘特圖
* **庫存管理部分：**
  * 直接設定有100個物品（同一種物品），接收來自樹梅派的訊息（代表從倉庫拿出一個物品），則MES也能同步更新物品剩餘數量
* **品質管理：**
  * 能接收來自品質檢測機台（樹莓派）的檢測數據，並顯示之
  * 品質管制圖繪製功能實作
* **資料分析及決策支援：**
  * 略
  
註：MES網站技術部分，本周已能顯示資訊為目標即可，不導入如Ajax、WebSocket等軟體技術