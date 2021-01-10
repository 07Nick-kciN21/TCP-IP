# STP(擴張樹協定)  
> **S** panning  
> **T** ree  
> **P** rotocol  
### 
> 當網路拓譜開始交錯出現迴圈，會造成廣播風暴，要避免這種狀況，就會關閉某些通道，把會通向自己的多個通道減到只剩一個，就像一棵大樹，每個部位都只有一個枝條連接。

## 步驟  
> 1.尋找作為root bridge的設備：
每台設備都有他的ID，ID最小的就是root bridge，如果ID相同，就看MAC ID。

> 2.在其他non-root-bridge設備上選出root port、Non-designated Port

> 3.選出每個VLAN的Designated Port、Non-designated Port

#### 想像一下

> 假設你家有前門跟後門，前門比後門更快到學校，那你就會走前門，關閉後門，但其他人會問你，後門對他們開放，你就會收"走那扇後門需要的"過路費，你家可能還有另一扇後門，但沒人詢問，就關著。  
> 如果兩家的過路費相同就選ID小的  
學校=root bridge  
前門=Root Port   
後門=Designated Port  
關閉的後門=Non-designated Port  
屬於那扇門的過路費=Transmission Cost  