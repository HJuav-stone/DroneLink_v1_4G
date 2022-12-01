# DroneLink_v1_4G
## 簡介
  ** 此版本為 4G固定IP 使用方式 提供基本數傳/圖傳功能 (相機必須為 IPCAM)
  1. [樹莓派映像檔下載連結](https://drive.google.com/file/d/19xRUBxFQBQ30wtv2cNePWVmsS-2G2PHl/view?usp=share_link)
  2. 樹莓派硬體: pi3/4
  3. 硬體連接方式 : 
      1. 樹莓派透過 ＵＳＢ轉　ＵＡＲＴ連接飛控之 Telem2孔位，　baudrate = 57600 (飛控需確定為此設定)
      2. IPCAM 之 ip 需設定成 10.3.141.50 才可以使用 , 在透過 ethernet 與樹莓派之ethernet 連接
  4. dongle 確認有連上網路後 即可用 dongle 之IP  來連線 , 數傳提供 udp : static ip:14550 / tcp :static ip : 5760  圖傳提供 rtsp://static:554 之通道
  
## 軟體調整方式
  1. 可 wifi 連線drone link  ssid :HJ_Dronelink pawwsord:12345678
  2. 透過 putty 連線 輸入 static ip 進行連線 user : pi password :123456
  3. 可調整 startup.sh 增加 udp 或 tcp 等 port 按需求調整
  "mavproxy.py --master=/dev/device1  --out=udpin:0.0.0.0:14550 --out=tcpin:0.0.0.0:5760 " # 可再增加依照此寫法 --out=udpin:0.0.0.0:14551 ... 增加
  5. 4G 連線 可調整 APN ,預設APN 為 internet
  透過登入Pi 輸入  
  `sudo nano /etc/ppp/peers/4GLTE`
  調整 如下圖  
  ![image](https://user-images.githubusercontent.com/104482291/205024995-2dcfd137-d852-44cf-8135-1ecbcf309394.png)
  框起來這行之 -T + internet 把 internet 改成想變之APN
  
  
  
  

