# 股市篩選爬蟲
最後更新日期 : 2022/07/05  
系統版本號 : V1.7.2  [^1]  
系統更新內容 : 
-改進代數自檢查機制 -改進Line Notify訊息通知格式  
[^1]: 歷史版本紀錄情詳: [Google表單連結](https://docs.google.com/spreadsheets/d/12K44nVoEXV6l2cOOBSFbIfZ-uMTvB-LIDd1cfHzQAgw/edit?usp=sharing)
## 前言
這個頁面存放的Python檔案，是我利用Python所製作的股票篩選爬蟲。  
此股票篩選爬蟲能夠協助我篩選有購買價值意義的股票。  
## 成效
在篩選爬蟲還在測試版前(6/10)，其股票勝利率約為81.13%[^2][^3]。  
期間最初購買日為(5/23)，最後購買日為(5/31)，最後清算日為(6/17)，實際股票持有期間將不超過一個月。  
[^2]: 股票勝利率試算期間為(5/23~5/31)期間有正常開市之日，由爬蟲於正常開市之日(n)篩選可購入股，並於當日以收盤價買入。試算方式暫不考慮是否得以實際購入，例如:隔日開盤漲/跌停或因特殊原因暫緩交易等…。
[^3]:賣出日說明:(因文字可能不好理解，建議您可以看圖文版:https://bacons.cc/d/3112 。
第一次賣出日為(n+2天正常開市日)日，若(n+2天正常開市日)日個股股價大於(n)日之收盤價，則賣出。反之，將續抱該個股至第二賣出日。
第二次賣出日為以一期間之最後交易日(m)，往下週找最後開市日(o)，若攤還日期間(m ~ o)，有大於(n)日之開盤價之日(q)者，則(q)日賣出。反之，將續抱該個股至第三賣出日。
第三次賣出日為以上週最後開市日(o)，往下週找最後開市日(r)，若攤還日期間(o ~ r)，有大於(n)日之開盤價者，則賣出。反之，全數於(n)日購入之股票於(r)日停損。
## 專案用法(尚未完成)
我將會在此專案分階段說明，我在製作爬蟲實的思路，以及每個階段參考的資料。  
由於篩選爬蟲尚不完美，因此也會繼續想方設法地完善它，還請教授們見諒。
