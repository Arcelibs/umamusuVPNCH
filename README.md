# umamusuVPNCH

**備註:使用AWS Lightsail**

優點就是前三個月免費(每月720小時)，後面每個月只要3.5USD，目前賽馬娘可以用AWS東京機房架設

**不考慮ACGPower或島風Go或其他加速器的原因**

單純玩遊戲可以，下載遊戲的速度慢到不行，受不了
> 不然ACGPower一個月只要10RMB那可以說是非常的便宜啊

**不考慮其他VPN的原因**

目前主流VPN連日線路都是被Ban，只能連歐洲或者東南亞，那個線路非常慢根本沒法順暢用

## 申請AWS Lightsail

選擇一台東京D區域的主機，D區域的IP連線比較穩定(?)

<img width="768" alt="截圖 2021-12-27 下午12 12 02" src="https://user-images.githubusercontent.com/49543451/147717785-a2b63cf5-c237-4a58-924f-28120abc403a.png">

選擇Linux OS Only，系統看個人喜好，這邊用Debian，然後按下Create

<img width="747" alt="截圖 2021-12-27 下午12 12 13" src="https://user-images.githubusercontent.com/49543451/147717751-8842eb03-8577-4154-9949-1e00b357d437.png">

申請需要一段時間，這時候來Network這邊建一個靜態外網IP，把他跟剛剛建立的主機串在一起，不這樣的話每次重啟後IP都會跑掉很麻煩

<img width="978" alt="截圖 2021-12-27 下午12 12 59" src="https://user-images.githubusercontent.com/49543451/147717855-be9dda61-67bc-4a26-b2a1-a849700f0d79.png">

<img width="770" alt="截圖 2021-12-27 下午12 13 51" src="https://user-images.githubusercontent.com/49543451/147717972-6b06f2f0-7004-40a7-99b1-0cc2a8400870.png">

防火牆的部分，加入UDP 1194 Port讓VPN可以通

<img width="787" alt="截圖 2021-12-27 下午12 16 04" src="https://user-images.githubusercontent.com/49543451/147718095-33ccf1bc-0105-4015-9af2-ad3cd81a8df7.png">


好了之後可以直接用瀏覽器SSH連線這台主機，當然如果你有喜歡的SSH工具也能用

Windows可以用Putty或者是XShell

MacOS的話可以用內建terminal

<img width="609" alt="截圖 2021-12-27 下午12 14 46" src="https://user-images.githubusercontent.com/49543451/147718039-bdbba859-2687-4845-9252-c72674447f26.png">


## SSH連線安裝

慣例先取得管理員權限
> Sudo -i

然後更新一下系統包，安裝Wget工具
> apt-get update

> apt-get install wget




<img width="865" alt="截圖 2021-12-27 下午12 18 38" src="https://user-images.githubusercontent.com/49543451/147718132-745cbbd4-1b22-400b-bdb6-128fafe98ff1.png">

