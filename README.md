# Product-Recommender-System
使用電商Olist提供的資料，建立產品推薦系統。<br/>
Data_link: <a href="https://www.kaggle.com/olistbr/brazilian-ecommerce/kernels">Brazilian E-Commerce Public Dataset by Olist</a>
<h4>目標</h4>
使用電商Olist提供的客戶資料、產品資料、訂單資料和購買評價，使用Turcreate套件進行產品推薦系統建立，為每個客戶提供10筆推薦產品。
<lo>
<li>資料筆數：112,650筆(資料整合後)</li>
<li>資料區間：2016/09/04~2018/09/93</li>
</lo>
<br/>
<h4>結論</h4>
<h5>a. RFM客戶模型</h5>	
	使用k-mean可以將客戶區分成六大群，其中重要保持的客戶為第一類：消費金額高的客人、第三類：消費金額高於平均，且頻率偏高、第五類：消費金額偏高，且頻率高；第六類：半年前進行消費的客戶。
<br/>
<img src="https://github.com/wu0up/Product-Recommender-System/blob/master/Picture/Customer_cluster.png">

<h5>b. 推薦模型評估</h5>
本次使用以下三種方法建置推薦系統模型，使用均方誤差根(RMSE)和精確度-召回率(Precision-Recall)評估模型；Cosine Similarity的誤差偏高，推測可能是因為我們只有客戶購買產品的資料，因此誤差較大；此外，Cosine Similarity的推薦項目沒有空值，因此選擇其為推薦模型。
<lo>
<li>Popularity-根據產品的熱門程度，推薦給使用者，不考量使用者的喜好。</li>
<li>Cosine Similarity-計算產品間的Cosine相似度，將和使用者購買產品最相近的推薦給使用者。</li>
<li>Pearson Similarity-計算產品的Pearson相似度，推薦和購買產品最相似的產品。</li>
</lo>
<img src="https://github.com/wu0up/Product-Recommender-System/blob/master/Picture/Model_comparison.png">
