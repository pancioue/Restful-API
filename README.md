關於restful api的優點，網路上可以找到很多資源，但大多都有一個共通的盲點  
就是一般的api形式也能辦到，而不是針對restful的優點  
以下整理出自己對restful api特點的理解:

### restful api:
1. 統一介面，基於http method，便於跨平台連接
2. 無狀態，其實用無記憶性可能更容易理解，每個request之間不須依賴其他request，每次都是獨立的。  
   更加有利於api的復用，於設計上多了很大的彈性跟延展性。同時也能減少server消耗在記憶狀態的loading。
3. 減少流量: 由於無狀態，不須依賴其他api，不需要經過多層轉跳之類的才能取得資源。
   
### 前後端分離優點: (restful由於也是前後端分離，說是restful的優點也沒錯)
* 可跨平台
* 與UI脫鉤，畫面渲染交由client端處理，方便程式設計
* 便於快取機制:  
  許多網站都有提到restful優點是便於快取機制，基本上可以確定不論是一般api或restful都能利用快取，  
  但目前並不知曉restful api是否有比一般api更加好利用於快取機制。

與UI脫鉤是否減少流量這點，個人暫時持保留態度  
如果要說因為跨平台，用web的改用app那的確可以大幅減少流量，  
但如果同樣是web來比較，可能還得仰賴於前端的設計才能有效減少流量。

參考:  
https://stackoverflow.com/questions/63722192/how-come-server-is-supposed-to-cache-information-in-rest-apis  
https://ithelp.ithome.com.tw/articles/10157674  
https://www.mulesoft.com/resources/api/top-3-benefits-of-rest-apis
