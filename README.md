# DroneLink_v1_4G
## 簡介
  ** 此版本為 4G固定IP 使用方式 提供基本數傳/圖傳功能 (相機必須為 IPCAM)
  1. [樹莓派映像檔下載連結](https://drive.google.com/file/d/19xRUBxFQBQ30wtv2cNePWVmsS-2G2PHl/view?usp=share_link)
  2. 樹莓派硬體: pi3/4
  3. 硬體連接方式 : 
      1.1. 樹莓派透過 ＵＳＢ轉　ＵＡＲＴ連接飛控之 Telem2孔位，　baudrate = 57600 (需確定)
      1.2. IPCAM 之 ip 需設定成 10.3.141.50 才可以使用 , 在透過 ethernet 與樹莓派之ethernet 連接
  4. dongle 確認有連上網路後 即可用 dongle 之IP  來連線 , 數傳提供 udp : static ip:14550 / tcp :static ip : 5760  圖傳提供 rtsp://static:554 之通道
  
## 軟體調整方式
  1. 可 wifi 連線drone link  ssid :HJ_Dronelink pawwsord:12345678
  2. 透過 putty 連線 輸入 static ip 進行連線 user : pi password :123456
  3. 可調整 startup.sh 增加 udp 或 tcp 等 port 按需求調整
  
  

