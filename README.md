# Currency_Identifier

---

## 機器學習Project
### 109321053 資工二 繆亭霄
### 109321054 資工二 林煒傑
### 109321040 資工二 林興政

---

## Project預覽
* ![image](https://github.com/CorgiCake/Currency_Identifier/blob/main/title.jpg)

---

## 語言環境
* 語言：Python 3.9
* 環境：CUDA : 11.1  
&emsp;&emsp;&emsp;cuDNN : 8.0.5  
&emsp;&emsp;&emsp;tensorflow : 2.8.0
       
## 圖片資料
* 國家種類：Iraqi, India, Nepal, HongKong, Taiwan
* 幣值種類：10, 20, 50, 100, 200, 500, 1000, 2000, 5000
* 雲端連結：https://drive.google.com/file/d/1W3CCQL19SmAmhOtUXP7k2P3bpHARbmNl/view?usp=sharing  
內包含圖片資料、模型權重、label.csv


---

## 操作說明
* Split_Data()  
  用於將資料切割為train與val，路徑已設定好，如有變動請對base_dir變數做調整
* Get_Data()  
  將資料用ImageDataGenerator對train做擴增，並將label對上各自分類，回傳train資料與val資料
* Create_model()  
  建立EfficientNet模型與輸出的全連接層，回傳模型
* Training(model, train, val)  
  訓練模型，參數輸入模型、train資料、val資料，回傳訓練完成的模型、訓練記錄
* Predict_single(model, image)  
  用於預測單張圖片，參數輸入模型、圖片路徑。圖片路徑請用image_path變數做調整(需加上.jpg)，路徑為.py檔的相對路徑。印出預測國家、預測幣值並畫出機率分布直方圖
* Predict_batch(model, dir)  
  用於預測多張圖片，參數輸入模型、圖片資料夾路徑。圖片資料夾路徑請用dir變數做調整，路徑為.py檔的相對路徑。印出預測出的分類，因圖片量過大可能導致輸出過多，預測結果將以int陣列表示，每種數字對應的國家與幣值請參照label.csv
* Save_weights(model)  
  儲存模型權重，參數輸入模型
* Load_Weights(model)  
  讀取模型權重，參數輸入模型，回傳更新權重後的模型
* Show_train_history(history)  
  將訓練過程使用折線圖畫出，參數輸入訓練紀錄

---

## 功能
* 預測紙幣國家、幣值

---

## 動機與目的
* 幫助盲人辨識紙幣
* 對大量紙幣進行分類
* 普及自動驗鈔機
* 普及無人化商店
