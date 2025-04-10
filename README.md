# QR Code base64 字串解碼
本項目希望利用程式自動化工作流程，快速處理公司內待處理的 QR Code ，以達到客戶端可以快速認證、傳遞與交換資料，透過程式自動化處理 QR Code 的方法，將 QR Code 內容彙整成單一的代辦工作清單，改善工作效率不佳的問題。資訊散布在許多不同的地方已成常態，提升效率的方法就是能快速將分散於各處的資訊進行彙整、分析與處理，各種 API 自動串接讓人力資源短缺的環境下，工作流程更流暢，自動處理例行工作瑣事也成為當今許多經營者首要的任務，讀取各網站自動生成 QR Code 的內容，以便進行下一個動作，最理想的做法是只要決策確認後，系統就能自動處理進行掃碼授權或者是掃碼繳費，完成接下來的所有工作，省去繁複的作業。


由於項目範圍很大，無法於短時間內解決所有企業所面臨的問題，在此僅針對 QR Code 內容進行文字輸出，之後可以根據 QR Code 的各種規範完成接下來應該要做的工作。這裏特別針對程式自動產生的 QR Code 進行處理，希望能藉此開啟開發者更多的發想與應用。許多網站或 API 以 data:image/png;base64 的形式提供 QR Code，提供許多的 APP 與行銷網頁可以呈現需要的 QR Code，如果開發者無法從 API 其他欄位取得條碼的原始資料獲更多資訊，只能先自動將條碼解碼再進行後續的其他處理，也許這裡提供的方法可以試試看。

![image](https://github.com/9do-service/b64PNGDecode/blob/main/demo.png)

開發環境，平台 Windows

pyhton 版本
Python 3.10.11 (tags/v3.10.11:7d4cc5a, Apr  5 2023, 00:38:17) [MSC v.1929 64 bit (AMD64)] on win32

安裝相關模組
pip install -r requirements.txt

執行
pyhton run.py

執行之後會啟動一個 server 並開啟瀏覽器，Text to Encode 可填入任意字串，按下產生 "產生 Base64 字串" 按鈕，會將字串會編碼產生 base64 的 QR Code 字串，模擬從其他 API 傳回 QR Code 影像，如果希望看到 QR Code 可以修改 index.html，將 #qrcode-hidden-renderer { display: none; 將 display: none; 加上註解，就會顯示該 QR Code 影像，該字串會顯示在 Generated Base64 PNG String 文字方框中，接下來按下 "將文字輸入框的資料解碼(測試版隨機加入 *)" 按鈕，會產生Generated Base64 PNG String 文字方框資料的解碼結果。

 
 
【贊助】
開發測試階段，有許多問題存在，若在使用上有發現問題，請告訴我，若對此感興趣可以合作
