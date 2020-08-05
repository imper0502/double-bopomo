# 雙碼注音

  給**注音**使用者的雙拼輸入法。學習高效率的雙拼輸入法之前不再需要額外學習漢語拼音。
  按鍵定位類似漢語拼音、通用拼音，但是拼音規則為注音的拼音規則。

## 鍵位圖
  ![KB layout](https://i.imgur.com/fXLonhD.jpg)
  按下【'】鍵，可以查詢佈局。 

## 說明
  目前，這是一個 Rime 輸入法引擎與 cin 碼表的輸入方案，需要安裝以下任何一款 Rime 輸入法（推薦）或其他可讀 cin 碼表的輸入法，方可使用：
  
  > - 可被 Rime 輸入法引擎讀取的「Rime 雙碼注音輸入法實作」要用什麼授權我還要研究一下。  
  看看是跟隨 rimelib(BSD-3-Clause), rime-terra-pinyin(LGPLv3), rime-double-pinyin(GPLv3)哪個方案
  > - cin 檔的實作是 **MIT** 授權。之後會分到別的 Repo
  
  > - 雙碼注音歡迎各種不同的輸入法實作。請保留作者。
  > - 雙碼注音的第一目標是【**普及率**】
  
  > - 雙碼注音是一種輸入法，不是檢字法。
  > - 不適合大量輸入人名這種需要*精確*定位到某個字的情況。

### Rime 輸入法列表   
  - [小狼毫](https://rime.im/download/)（官方，Windows）【[如何安裝與設定](https://github.com/imper0502/rime-double-bopomo/wiki/%E5%A6%82%E4%BD%95%E5%AE%89%E8%A3%9D%E8%88%87%E8%A8%AD%E5%AE%9A%EF%BC%9F#%E5%B0%8F%E7%8B%BC%E6%AF%AB)】
  - [Prime](https://github.com/osfans/PRIME/releases)（Windows）
  - [Pime](https://github.com/EasyIME/PIME/releases)（Windows）
  - [鼠鬚管](https://rime.im/download/)（官方，macOS）
  - [XIME](https://github.com/stackia/XIME)（macOS）
  - [ibus-rime](https://rime.im/download/)（Linux，官方，推薦）
  - [Fcitx-rime](https://github.com/fcitx/fcitx-rime)（Linux，推薦）
  - [同文輸入法](https://github.com/osfans/trime/releases)（Android）
  - [Emacs Rime](https://github.com/DogLooksGood/emacs-rime)
  - iRime（iPhone, iOS）【[如何安裝與設定](https://github.com/imper0502/rime-double-bopomo/wiki/%E5%A6%82%E4%BD%95%E5%AE%89%E8%A3%9D%E8%88%87%E8%A8%AD%E5%AE%9A%EF%BC%9F#irime)】

### 輸入規則   
  1. 兩碼一字：第一碼聲母，第二碼韻母。（第三碼可用數字１～５輸入聲調，第三碼非必要，可省略。）
  2. 虛韻母：ㄓㄔㄕㄖ　ㄗㄘ厶  這些可以獨存的聲母（其實是韻母省略）要多打一個虛韻母「ㄭ」在後。  「ㄭ」放在 `I 鍵`上，用 emoji: 😬 表示，因爲發音時嘴形類似。
  3. 0️⃣聲母：介音與所有的韻母（ㄧㄨㄩ、ㄚㄛㄜㄝ、ㄞㄟㄠㄡ、ㄢㄣㄤㄥ及兒化韻母ㄦ）獨存時，先按零聲母，再按對應的按鍵。  零聲母放在 `E 鍵`上，用 emoji: 🈳/0️⃣ 表示，因爲`Empty`。
  
  如此，所有的注音符號音節（但不包括尖團音），全部編碼成兩碼了。
  另外，目前是12345輸入聲調，但聲調不是必要的；67890選字。
  此外，ㄗ放 `W 鍵`的設計，參考了法語鍵盤（azerty keyboard）`Z 鍵` `W 鍵` 交換的設計。
#### 輸入範例與比較
  ||我|用|雙|碼|注|音|輸|入|中|文|漢|字|
  |--|--|--|--|--|--|--|--|--|--|--|--|--|
  |雙碼注音|uo|yf|oc|ma|au|id|ou|ru|al|ud|hk|wi|
  |微軟注音|ji3|m/4|gj;␣|a83|5j4|up␣|gj␣|bj4|5j/␣|jp6|c04|y4|
  |微軟拼音|wo|yong|shuang|ma|zhu|yin|shu|ru|zhong|wen|han|zi|
  |漢語拼音|wǒ|yòng|shuāng|mǎ|zhù|yīn|shū|rù|zhōng|wén|hàn|zì|
  |注音符號|ㄨㄛˇ|ㄩㄥˋ|ㄕㄨㄤ|ㄇㄚˇ|ㄓㄨˋ|ㄧㄣ|ㄕㄨ|ㄖㄨˋ|ㄓㄨㄥ|ㄨㄣˊ|ㄏㄢˋ|ㄗˋ|

#### 其他應用
  - 點字
  - 旗語
  - 手語

### 簡拼規則
正常輸入時，若遇到雙拼空碼、奇數輸入鍵時，就會有簡拼。（Rime設計理念：假設使用者所有輸入的按鍵都是正確的。）
以下提供**一定**被視為簡拼的方法：
  1. 注音聲母（或大寫一碼韻母） + 聲調（數字１～５）；所以改用６～０選字（預設一頁五字）  
     **e.g.** ➡️ `o1r4k4l4`➡️ `ㄕˉㄖˋㄎˋㄌˋ`➡️ 生日快樂
  2. 注音聲母（或大寫一碼韻母） + 分詞鍵【'】（【'】在分號鍵的右邊。）  
     **e.g.** ➡️ `o'r'k'l'`➡️ `ㄕ'ㄖ'ㄎ'ㄌ'`➡️ 生日快樂
  3. 按下【;】後，強制使用簡拼。
     **e.g.** ➡️ `;orkl`➡️ `ㄕ　ㄖ　ㄎ　ㄌ`➡️ 生日快樂
     > ⚠️若【;】有設定額外功能，則會衝突不可使用。
	
### 其他規則（不知道也不影響正常使用）
  1. ㄧㄨㄩ ㄚㄛㄜㄝ ㄞㄟㄠㄡ ㄢㄣㄤㄥ ㄦ 也可以直接 `Shift` + 【對應按鍵】，效果和「輸入規則 3.」相同。**簡拼模式時非常有用。**
  2. 預設使用聲調當**輔助碼**  
     `雙拼 + 【;a】 = 一聲；1 向下移動2排`  
     `雙拼 + 【;s】 = 二聲；2 向下移動2排`  
     `雙拼 + 【;d】 = 三聲；3 向下移動2排`  
     `雙拼 + 【;f】 = 四聲；4 向下移動2排`  
     `雙拼 + 【;】  = 輕聲；`	 
     手機上的Rime可能無法直接輸入聲調，這是設計給這種情況用的。
  3. 不知道如何拼的字，按下【`】後，使用**倉頡**查詢雙碼注音。
     > ⚠️可以自行替換反查的輸入法
  
### 學習指引（銜接方案）
  可以先從[全碼注音](https://github.com/imper0502/rime-full-bopomofo) —— `full_bopomofo.schema.yaml`，這個銜接方案開始。這個方案沒有結合韻；保留0️⃣聲母、😬韻母。  
  - ㄓㄔㄕㄖ ㄗㄘㄙ 有輸入聲調時，可以省略😬韻母。  
  - ㄧㄨㄩ 有輸入聲調時，可以省略0️⃣聲母。  
  - 聲調可以省略。
  - 聲調放鍵盤的下排中央，建議用大拇指擊鍵，並只在必要時使用聲調輔助輸入。
  ![full bopomofo KB layout](https://i.imgur.com/dskVzSG.jpg)
  
### 檔名解釋
  - `double_bopomo.schema.yaml`：Rime 輸入方案檔，字典檔使用 Rime 內建的「地球拼音」字典檔，使之與「地球拼音」、「注音」等方案共用詞庫。
  - `abbreviated_bopomo.schema.yaml`：Rime 輸入方案檔，縮寫注音，雙碼注音的簡拼模式。  
    > ⚠️需要使用簡拼模式的使用者，請務必把`abbreviated_bopomo.schema.yaml`跟`double_bopomo.schema.yaml`**一起**放到 Rime 的使用者資料夾裡面。並編輯自己的使用者設定檔。【[如何安裝與設定](https://github.com/imper0502/rime-double-bopomo/wiki/%E5%A6%82%E4%BD%95%E5%AE%89%E8%A3%9D%E8%88%87%E8%A8%AD%E5%AE%9A%EF%BC%9F#%E5%B0%8F%E7%8B%BC%E6%AF%AB)】  
    > ⚠️若是不使用簡拼的使用者，這個檔案就不用放到使用者資料夾。
  - `RIME 設定範例／cangjie.yaml`：需要使用倉頡輸入法當輔助輸入法的人，請參考。【預設】
  - `RIME 設定範例／pinyin.yaml`：需要使用拼音輸入法當輔助輸入法的人，請參考。
  ---
  - `double_bopomo_keyboard_layout.jpg`：雙碼注音的基本鍵盤佈局圖。
  - `TRIME 設定範例／trime.custom.yaml`：同文輸入法鍵盤設定檔。
  - `CIN 碼表／BIG5_double_bopomo.cin`：大五碼雙碼注音 + 大五碼「三碼」注音 CIN 檔（雙碼注音 + 一碼聲調（數字））。
  - `CIN 碼表／CNS_double_bopomo.cin`：全字庫雙碼注音 + 全字庫「三碼」注音 CIN 檔（雙碼注音 + 一碼聲調（數字））。 
  - `README.md`：本檔案。

## 相關連結
  - [Youtube影片](https://youtu.be/SD2iaUONg7A)
  - [PTT發佈頁、討論頁](https://www.ptt.cc/bbs/IME/M.1572622340.A.FEA.html)

## 截圖
  > <img src="https://i.imgur.com/9hi4wRF.jpg" width="50%"><img src="https://i.imgur.com/oPuEzOj.jpg" width="50%">  
  左圖使用同文輸入法 on Android，右圖使用 iRime on iOS。
  
  > ![同文輸入法鍵盤](https://i.imgur.com/AEGzJVi.png)  
  上圖是目前提供的同文輸入法鍵盤[設定檔](https://github.com/imper0502/rime-double-bopomo/blob/master/trime.custom.yaml)的截圖。
  
  > ![使用 fcitx-rime on kde](https://imgur.com/DS9ZpnG.jpg)  
  使用 fcitx-rime on kde
  
  > ![Heatmap](https://imgur.com/UUiUJxB.jpg)  
  鍵盤熱力圖
  
## 網友提供的相關圖片
  > ![Layout by xcv123321](https://i.imgur.com/xq0NrR6.png)  
  由[xcv123321](https://github.com/xcv123321)提供的雙碼注音按鍵佈局圖
  
  > ![Heatmap by jamessa](https://i.imgur.com/N1o1J4K.jpg)  
  由[jamessa](https://github.com/jamessa)提供的雙碼注音按鍵熱力圖，這是詳細的[分析結果](http://patorjk.com/keyboard-layout-analyzer/#/load/p6bsg5Fx)
  
## 銘謝
  1. [Rime](https://rime.im/) 輸入法引擎開發者 [佛振](https://github.com/lotem) 先生及所有貢獻者。
  2. [gugod](https://github.com/gugod) 協助刪除CIN檔重複的字詞.
