# Currency_Identifier

---

## 機器學習Project
### 109321053 資工二 繆亭霄
### 109321054 資工二 林煒傑
### 109321040 資工二 林興政

---
## 示範影片
* [操作影片連結](https://youtu.be/SH1grgiGaM4)
  ![image](https://github.com/CorgiCake/Logic-Design-Final-Project/blob/main/final.jpeg)


## 語言環境
* 語言：Python3.9
* 環境：CUDA:11.1
       cuDNN:8.0.5
       tensorflow:2.8.0


---

## 操作說明
* Split_Data()
  用於將資料切割為train與val, 路徑已設定好, 如有變動請對base_dir變數做調整
* Get_Data()
  將資料用ImageDataGenerator對train做擴增，並將label對上各自分類，回傳train資料與val資料
* Create_model()
  建立EfficientNet模型與輸出的全連接層，回傳模型
* Training(model, train, val)
  訓練模型，參數輸入模型、train資料、val資料，回傳訓練完成的模型、訓練記錄
* Predict_single(model, image)
  用於預測單張圖片，參數輸入模型、圖片路徑，圖片路徑請用image_path變數做調整(需加上
  .jpg)，印出預測國家、預測幣值並畫出機率分布直方圖
* Predict_batch(model, dir)
  用於預測多張圖片，參數輸入模型、圖片資料夾路徑，圖片資料夾路徑請用dir變數做調整，印出預測出的分類，因圖片量過大可能導致輸出過多，預測結果將以int陣列表示，每種數字對應的國家與幣值請參照label.csv
* Save_weights(model)
  儲存模型權重，參數輸入模型
* Load_Weights(model)
  讀取模型權重，參數輸入模型，回傳更新權重後的模型
* Show_train_history(history)
  將訓練過程使用折線圖畫出，參數輸入訓練紀錄

---

## 功能
*	最上方隨機位置掉落敵方飛機
*	我方飛機使用激光攻擊敵方飛機，打中即可加一分，分數達十分勝利
*	吃到補給品 (藍色球) 可以充能強化激光
*	激光有冷卻時間，與強化激光冷卻分開計算
*	被敵人碰撞後，血量扣一，血條歸零遊戲失敗
*	勝利後出現 “ V I C T O R Y ” 在 RGB 顯示器上
*	失敗後出現 “ D E F E A T ” 在 RGB 顯示器上
*	遊戲配樂為 “ 紅蓮的弓矢 ” & “ 妖精的尾巴 ”
*	遊戲難度影響飛機掉落速度，多種難度皆為開啟時，以較難者為優先
*	難度全關即為暫停
*	Reset 開啟，即可重新遊戲
