## RESTful api優點:
1. 無狀態:
   其實用無記憶性可能更容易理解，每個request之間不須依賴其他request，每次都是獨立的。  
   有利於api的復用，於設計上多了很大的彈性跟延展性。同時也能減少server消耗在記憶狀態的loading。
2. 減少流量: 由於無狀態，不須依賴其他api，不需要經過多層轉跳之類的才能取得資源。
3. 統一命名，無需再為密名而苦惱
4. 統一介面，資源存取基於http method，加上無狀態的特性，便於跨平台連接
   (這點很抽象，一直在猶豫要不要拿掉，不過我想對於串接的人來說，看到restful應該會比看到一般的api要來得舒服些)
   
## 前後端分離優點:
restful也是前後端分離，說是restful的優點也沒錯
* 可跨平台
* 與UI脫鉤，畫面渲染交由client端處理，方便程式設計
* 便於快取機制:  
  許多網站都有提到restful優點是便於快取機制，基本上可以確定不論是一般api或restful都能利用快取，  
  但目前並不知曉restful api是否有比一般api更加好利用於快取機制。


與UI脫鉤是否減少流量這點，個人暫時持保留態度  
如果要說因為跨平台，用web的改用app那的確可以大幅減少流量，  
但如果同樣是web來比較，可能還得仰賴於前端的設計才能有效減少流量。


## 觀點
過去一直以為只要符合http verb就是restful了，如果以這種定義來說，其實無狀態這特性，一般的api也能辦到。  
但實際上restful的風格不應該只是符合http verb，對應的資源操作才是restful的核心理念。  
可以說基於http verb只是一種表現，資源導向才是restful的真正意涵。  
雖然說一般的api也能設計成無狀態，但在restful問世以前，一般的api設計並沒有資源導向的概念，應該也鮮少有人會遵從無狀態設計吧。  

#### 結語
__資源導向的設計風格，讓restful api具有無狀態的特性，且更符合物件導向設計理念__


- - - 
參考:  
https://stackoverflow.com/questions/63722192/how-come-server-is-supposed-to-cache-information-in-rest-apis  
https://ithelp.ithome.com.tw/articles/10157674  
