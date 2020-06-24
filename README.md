# 雙碼注音
## 簡介
  給注音使用者的雙拼輸入法。不需要額外學習漢語拼音。

## 鍵位圖
  ![KB layout](https://github.com/imper0502/rime-double-bopomo/blob/readme-editor/double_bopomo_keyboard_layout.jpg)

## 說明
  目前，這是一個 Rime 輸入法引擎與 cin 碼表的輸入方案，需要安裝以下任何一款 Rime 輸入法（推薦）或其他可讀 cin 碼表的輸入法，方可使用：

### Rime 輸入法列表   
  - 小狼毫（官方，Windows）【[如何安裝與設定](https://github.com/imper0502/rime-double-bopomo/wiki/%E5%A6%82%E4%BD%95%E5%AE%89%E8%A3%9D%E8%88%87%E8%A8%AD%E5%AE%9A%EF%BC%9F#%E5%B0%8F%E7%8B%BC%E6%AF%AB)】
  - Prime（Windows）
  - 鼠鬚管（官方，macOS）
  - XIME（macOS）
  - ibus-rime（Linux，官方，推薦）
  - Fcitx-rime（Linux，推薦）
  - 同文輸入法（Android）
  - iRime（iPhone, iOS）

### 輸入規則   
  1. 兩碼一字：第一碼聲母，第二碼韻母。（第三碼可用數字１～５輸入聲調，第三碼非必要，可省略。）
  2. 虛韻母：ㄓㄔㄕㄖ　ㄗㄘ厶  這些可以獨存的聲母（其實是韻母省略）要多打一個虛韻母「ㄭ」在後，ㄭ放在I鍵上，用 emoji: 😬 表示，因爲發音時嘴形類似。
  3. 零聲母：所有的韻母都可以獨存 ㄧㄨㄩ ㄚㄛㄜㄝ ㄞㄟㄠㄡ ㄢㄣㄤㄥ 及兒化音。
  
  如此，所有的注音符號音節（但不包括尖團音），全部編碼成兩碼了。
  另外，目前是12345輸入聲調，但聲調不是必要的；67890選字。此外，ㄗ放 W的設計，參考了法語鍵盤（azerty keyboard）。
 
### 簡拼規則
  1. 注音 + 聲調（數字１～５）；所以改用６～０選字（預設一頁五字）  
    `e.g.`➡️ **o1r4k4l4** ➡️ㄕˉㄖˋㄎˋㄌˋ➡️生日快樂
  2. 注音 + 分詞鍵【'】（【'】在分號鍵的右邊。）  
    `e.g.`➡️ **o'r'k'l'** ➡️ㄕ'ㄖ'ㄎ'ㄌ'➡️生日快樂
  3. 按下【;】後，強制使用簡拼。  
    `e.g.`➡️ **;orkl** ➡️ㄕ　ㄖ　ㄎ　ㄌ➡️生日快樂
  > ⚠️若【;】有設定額外功能，則會衝突不可使用。
	
### 其他規則（不知道也不影響正常使用）
  1. ㄧㄨㄩ ㄚㄛㄜㄝ ㄞㄟㄠㄡ ㄢㄣㄤㄥ ㄦ 也可以直接 `Shift` + 【對應按鍵】，效果和「輸入規則 3.」相同。**簡拼模式時非常有用。**
  
### 檔名解釋
  - `double_bopomo.schema.yaml`：Rime 輸入方案檔，字典檔使用 Rime 內建的「地球拼音」字典檔，使之與「地球拼音」、「注音」等方案共用詞庫。
  - `double_bopomo_vocabulary.schema.yaml`：Rime 輸入方案檔，雙碼注音的簡拼模式。  
    > ⚠️請務必把它跟`double_bopomo.schema.yaml`【一起】放到 Rime 的使用者資料夾裡面。
  - `cangjie.yaml`：需要使用倉頡輸入法當輔助輸入法的人，請參考。
  - `pinyin.yaml`：需要使用拼音輸入法當輔助輸入法的人，請參考。
  ---
  - `double_bopomo_keyboard_layout.jpg`：雙碼注音的基本鍵盤佈局圖。
  - `trime.custom.yaml`：同文輸入法鍵盤設定檔。
  - `CNS_double_bopomo_NO_tone.cin`：全字庫雙碼注音 CIN 檔。
  - `CNS_double_bopomo_with_tone.cin`：全字庫「三碼」注音 CIN 檔，雙碼注音 + 一碼聲調。
  - `README.md`：本檔案。

## 相關連結
  [PTT發佈頁、討論頁](https://www.ptt.cc/bbs/IME/M.1572622340.A.FEA.html)

## 截圖
  ![使用同文輸入法 on Android](https://i.imgur.com/9hi4wRF.jpg)
  ![使用 iRime on iOS](https://i.imgur.com/oPuEzOj.jpg)
  > ![同文輸入法鍵盤](https://i.imgur.com/AEGzJVi.png)  
  此圖是目前提供的同文輸入法鍵盤設定檔的截圖。
  
  ![使用 fcitx-rime on kde](https://imgur.com/DS9ZpnG.jpg)
  ![Heatmap](https://imgur.com/UUiUJxB.jpg)
  
## 網友提供的相關圖片
  > ![Layout by xcv123321](https://i.imgur.com/xq0NrR6.png)  
  由[xcv123321](https://github.com/xcv123321)提供的雙碼注音按鍵佈局圖
  
  > ![Heatmap by jamessa](https://scontent.frmq2-1.fna.fbcdn.net/v/t1.0-9/104496831_10158749532160616_3681282552113193519_n.jpg?_nc_cat=108&_nc_sid=ca434c&_nc_ohc=Ji2vM0ghxH0AX9E10KW&_nc_ht=scontent.frmq2-1.fna&oh=83075bc353b082084a15d74d6f5e147f&oe=5F0DD051)  
  由[jamessa](https://github.com/jamessa)提供的雙碼注音按鍵熱力圖
  
## 銘謝
  1. [Rime](https://rime.im/) 輸入法引擎開發者 [佛振](https://github.com/lotem) 先生及所有貢獻者。
