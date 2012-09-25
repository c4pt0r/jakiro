#Jakiro
<small>yet another distributed nosql database</small>

###About

---
jakiro是一個分佈式key-value db，採用c和python編寫，作爲我個人的練習的開源項目，旨在真正讓我理解一個分佈式系統之構成和運轉。jakiro的設計思想是簡單和嚴格的分層，我會盡力做到層間耦合最小，目標是能達到服務無縫的水平擴展和最終一致性。

第一步，在前端jakiro提供一個滿足memcached協議的服務，用普通的memcached客戶端即可訪問，作爲一個非工業級別的項目，目前暫時只提供set, get, delete，stat方法；或者提供一些http訪問的接口

第二步，路由層會用c或者python實現一個基於tcp的dht（分佈式hash table）服務供前端調用，這部分的設計也會嚴格的保證可水平擴展，不會存在單點的問題。

再之，單機的存儲會採用leveldb，採用hash-tree實現數據replication

###Docs

---
TBD

###Source

---
TBD


###參考

---
* douban Inc, BeansDB
* Amazon, Dynamo
* memcached

