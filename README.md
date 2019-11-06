## DocumentManager
### How to install and start
- pipenv shell
- pipenv install
- py main.py

## SPEC
### 主要為提供一文件內容管理功能，文件內容有不同類型，依類型顯示與操作亦有所差異
#### 文件資料夾管理(左側)
- 左側以樹狀結構呈現資料夾項目與其層級關系
- 新增：新增一個頂級資料夾
- 更新：更新選定頂級資料夾的名稱
- 刪除：刪除選定的整份頂級資料夾
- 匯入專案：匯出檔匯入文件內容管理器(格式待確認)
- 匯出專案：將選定物件匯出成檔案
- 匯出檔案：將文件內容匯出成 HTML
#### 文件物件管理(右上使用類似檔案總管的方圖呈現，依不同類型圖標不同)
- 「文件物件管理」以類似檔案總管的方式管理文件內容，功能包括新增、更新、刪除各類型文件物件。
- 文件物件類型分為資料夾(或稱段落 Section)、文字(Text)、數學(Mathml)三類。資料夾物件為可再包含各類型物件(資料夾、文字、數學)，文字物件為文字資訊，數學物件為以 MathML 撰寫的數學資訊。
- 點擊特定物件(滑鼠點兩下、鍵盤按 enter、右鍵第一個選項)
	* 進入：資料夾物件進入該資料夾內
	* 編輯：文字物件進行編輯：跳對話框給使用者修改文字物件內容，對話框內為文字物件內容的輸入框
	* 編輯：數學物件進行重寫：跳對話框給使用者重輸數學物件內容，對話框內為空的輸入框
- 路徑：顯示當前完整路徑
- 上一層(滑鼠點上一層按鍵、back space)：回到上一層資料夾
- 在右上物件上點選滑鼠右鍵或快顯鍵(標準鍵盤在右側ctrl的左邊)出現的選單項目
	* 進入或編輯，參考點擊物件區域的說明
	* 匯出(資料夾才有)：匯出選定資料夾內的物件內容成 html，需將資料夾內的物件按順序逐一輸出成 html 並連接起來，固資料夾內物件順序是有意義會影響輸出結果
	* 上一層(滑鼠點上一層按鍵、back space)：回到上一層資料夾
	* 前移(ctrl+shift+向左鍵)：將選定物件向前移動
	* 後移(ctrl+shift+向右鍵)：將選定物件向後移動
	* 新增：新增一個空文件物件，跳對話框選擇 type 與輸入 label，完成後新增於選定物件的後一項，無選定物件則新增於最末項
	* 更新(F2)：更新選定物件的 label
	* 刪除：刪除選定物件
	* 綜合輸入：跳對話框有一編輯框可輸入混合文字與數學的內容，完成後自動切割轉換成序列物件，新增於選定物件的後一項，無選定物件則新增於最末項(參考 integrate.py)
- 路徑切換(右上內容改變)後自動將焦點移到右上物件列表上
#### 文件物件內容管理(右下)
- 資料夾物件
    * 內容呈現：顯示資料夾內的各類型文件數量。
- 文字物件
	* 內容呈現：顯示文字內容
- 數學物件
	* 內容呈現：顯示數學樹狀結構
	* 互動：與該數學內容進行導航瀏覽，亦即可部份瀏覽數學內容中的子內容並在子內容間移動或縮放子內容大小(需待整合至 NVDA 內後使用 API 處理)
	* 複製：將內容複製到剪貼簿(需待整合至 NVDA 內後使用 API 處理)
- 各類型的內容呈現待瀏覽器整合內崁功能可行後會再進行設計調整