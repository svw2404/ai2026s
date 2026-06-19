# HW06 完整轉錄 (Full Transcription)

---

## PPT 1: HW06穩定擴散 (1).pptx — 作業說明 (14 slides)

---

### Slide 1 — 封面 (Title)
- 生成式人工智慧導論 114-2
- HW06 穩定擴散
- 鄭傳脩
- 國立臺北科技大學資訊工程系

---

### Slide 2 — 目錄
（僅目錄標題，無展開內容）

---

### Slide 3 — 目錄（展開）
目錄項目：
- 評分標準
- 作業說明
- 繳交資訊

---

### Slide 4 — 章節分隔：評分標準
章節 05 / 02

---

### Slide 5 — 評分標準 (Scoring)

| 難度 | 分數 | 說明 |
|------|------|------|
| Simple baseline | 4pt | Comfy UI 環境設定完成（需使用自己的 CheckPoint 和 LoRA） |
| Medium baseline | 4pt | 生成角色的圖片 |
| Strong baseline | 2pt | 生成完整角色動畫 |

總分：10pt

---

### Slide 6 — 章節分隔：作業說明
章節 05 / 03

---

### Slide 7 — Simple baseline (4pt)

**標題：** Simple baseline (4pt)  
**內容：** Comfy UI 環境設定完成

**圖片 1 (slide07_img1.png)：** 終端機（Terminal）顯示 pinggy 隧道已連線，輸出兩個 URL（Endpoint IP 和 ComfyUI 網址）

**圖片 2 (slide07_img2.png)：** ComfyUI 完整 AnimateDiff「文生影片」工作流截圖：
- 分頁名稱：文生影片
- 所有 23 個節點已連接完成，無紅框錯誤
- 顯示「Queue Prompt」按鈕和「Job completed」狀態

---

### Slide 8 — Medium baseline (4pt)

**標題：** Medium baseline (4pt)  
**內容：** 生成角色的圖片

**圖片 (slide08_img1.png)：** 示範生成的靜態圖片（角色圖）：
- 動漫少女，淺棕色頭髮，雙馬尾/小髮包
- 藍色長袖短版上衣，粉色碎花裙
- 手提藤編籃子，站在樹叢小徑上
- 背景：綠樹 + 木柵欄，全身構圖

---

### Slide 9 — Strong baseline (2pt)

**標題：** Strong baseline (2pt)  
**內容：** 生成完整角色動畫

**GIF (slide09_img1.gif)：** 範例動畫（四季換裝）：
- 第一幀（春）：同上少女，藍色上衣 + 粉色碎花裙，在花園小徑上，表情開心
- 動畫循環：春（碎花裙）→ 夏（短袖洋裝）→ 秋（毛衣+牛仔褲）→ 冬（羽絨外套）
- 共約 110 幀，frame_rate=8fps

---

### Slides 10 — 章節分隔：繳交資訊
章節 06 / 04

---

### Slide 11 — Regulations

> You should finish your homework on your own.  
> Do not share your codes with any living creatures.  
> Your HW will get 0 pt if you violate any of the above rules.  
> Professor & TAs preserve the rights to change the rules & grades.

---

### Slide 12 — Regulations（遲交規定）

作業遲交，分數打五折

---

### Slide 13 — 章節分隔：助教聯絡資訊
章節 07 / 05

---

### Slide 14 — 助教聯絡資訊 (TA Contact)

| 項目 | 內容 |
|------|------|
| TA | 賴秋彤 |
| TA Email | t114598033@ntut.org.tw |
| Email 主旨格式 | [ai2026s-hwX-學號] |

---
---

## PPT 2: 06-穩定擴散_文生圖生影片 (1).pptx — 課程講義 (42 slides)

---

### Slide 1 — 封面 (Title)
- 生成式人工智慧導論
- 06 穩定擴散
- 鄭傳脩
- 國立臺北科技大學資訊工程系

---

### Slide 2 — 章節分隔：使用模型
章節 01

---

### Slide 3 — 使用模型 01：Checkpoint based66_v30

**標題：** Civitai  
**副標題：** Checkpoint：based66_v30

**圖片 (slide03_img1.png)：** Civitai 模型頁面：
- 模型名稱：based66_v30
- 類型：CHECKPOINT MERGE
- 基底模型：SD 1.5
- 文件大小：1.99 GB
- 版本：v30

---

### Slide 4 — 使用模型 02：LoRA chibi-laugh

**標題：** Civitai  
**副標題：** LoRA: chibi-laugh

**圖片 (slide04_img1.png)：** Civitai 模型頁面：
- 模型名稱：Gyate Gyate chibi laugh 直接开笑
- 類型：LoRA
- 基底模型：SD 1.5
- 文件大小：144.12 MB
- 觸發詞（Trigger Words）：`chibi.laughing`
- 描述：賦予角色 chibi 笑臉動態表情

---

### Slide 5 — 使用模型 03：LoRA boldline

**標題：** Civitai  
**副標題：** LoRA: boldline

**圖片 (slide05_img1.png)：** Civitai 模型頁面：
- 模型名稱：boldline
- 類型：LoRA
- 基底模型：SD 1.5
- 功能：調整畫面線條粗細（加粗/去粗線）

---

### Slide 6 — 章節分隔：雲端運行
章節 02

---

### Slide 7 — Civitai 帳號設定

**標題：** Civitai  
**內容：** Civitai，一個開放模型下載的網站，可以上去下載任意你想要的模型。創建帳號後，點擊頭像 → Account Settings

**圖片 (slide07_img1.png)：** Civitai 帳號下拉選單：
- 使用者名稱：t113598022949
- ⚡ 100 Buzz 點數
- 選單項目：Your Profile / Training / My Collections / Liked Models / Bookmarked Articles / My Bounties / Buzz Dashboard / My Vault / Leaderboard / Auctions / Download Link App
- 底部圖示：燈光模式 / 設定（齒輪）/ 登出

---

### Slide 8 — Civitai 建立 API Key（位置）

**標題：** Civitai  
**內容：** 移到最下面，找到 API Keys，選擇 Add API Key

**圖片 (slide08_img1.png)：** Account Settings 頁面：
- "API Keys" 區塊，右上角有「+ Add API key」按鈕
- 說明文字：「You can use API keys to interact with the site through the API as your user. These should not be shared with anyone.」
- 空白狀態：「There are no API keys in your account / Start by creating your first API Key to connect your apps.」
- 底部另有「Refresh my Session」功能區塊

---

### Slide 9 — Civitai 建立 API Key（操作）

**標題：** Civitai  
**內容：** 隨意命名，API Key 出現的時候也記得要複製

**圖片 1 (slide09_img1.png)：** 「Create API Key」對話框：
- Name 欄位（必填 *）
- 佔位符：「Your API Key name」
- 按鈕：Cancel / Save（藍色）

**圖片 2 (slide09_img2.png)：** API Key 已建立的對話框：
- 標題：「Here is your API Key:」
- 顯示 Key（範例）：`769e1eae38e21b6b739e1916fe8d3ba8`
- 右側複製按鈕（剪貼板圖示）
- 警告：「Be sure to save this, you won't be able to see it again.」

---

### Slide 10 — Colab 程式碼下載

**標題：** Colab  
**內容：** Colab 程式碼下載連結

**圖片 (slide10_img1.png)：** GitHub 倉庫頁面 — text-to-video（Public）：
- 擁有者：lctung（教授帳號）
- 分支：main，1 Branch，0 Tags，3 Commits
- 檔案：README.md、Text_to_Video.ipynb
- README 標題：「Text to Image」
- README 說明：「利用 Civitai 上的開源模型（Based on Stable Diffsion），生成芙莉蓮和欣梅爾的圖片」
- 【Open in Colab】按鈕（Colab 徽章）

---

### Slide 11 — Colab Cell 1：啟動環境

**標題：** Colab  
**內容：** 安裝 Comfy UI 所需要的套件

**圖片 (slide11_img1.png)：** Colab 筆記本 —「第一步：啟動系統」：
- 說明：「這一步是安裝 ComfyUI 和常用插件 / 運行時間大約是 1-5 分鐘，取決於你的網絡連結情況」
- 注意：「Git clone the repo and install the requirements.（ignore the pip errors about protobuf）」
- 注意：「USE_GOOGLE_DRIVE 若有需要保存才需勾選」

```python
# #@title Environment Setup

from pathlib import Path

OPTIONS = {}

USE_GOOGLE_DRIVE = False  #@param {type:"boolean"}
UPDATE_COMFY_UI = True    #@param {type:"boolean"}
USE_COMFYUI_MANAGER = True  #@param {type:"boolean"}
INSTALL_CUSTOM_NODES_DEPENDENCIES = True  #@param {type:"boolean"}
OPTIONS['USE_GOOGLE_DRIVE'] = USE_GOOGLE_DRIVE
OPTIONS['UPDATE_COMFY_UI'] = UPDATE_COMFY_UI
OPTIONS['USE_COMFYUI_MANAGER'] = USE_COMFYUI_MANAGER
OPTIONS['INSTALL_CUSTOM_NODES_DEPENDENCIES'] = INSTALL_CUSTOM_NODES_DEPENDENCIES

current_dir = !pwd
WORKSPACE = "/content/ComfyUI"

if OPTIONS['USE_GOOGLE_DRIVE']:
    !echo "Mounting Google Drive..."
    %cd /
    from google.colab import drive
    drive.mount('/content/drive')
```

---

### Slide 12 — Colab Cell 2：Civitai Token

**標題：** Colab  
**內容：** 將 Civitai API Key 貼上

**圖片 (slide12_img1.png)：** Colab 程式碼儲存格：
```python
## 把你的 huggingface token 和 civitai token 拷貝在下面

# 用你的 civitai token 替換 XYZ
CIVITAI_TOKEN = "XYZ"

print("***** 你的token已經被應用到臨時變量中 ✅ ! ")
print("civitai token: ", CIVITAI_TOKEN)
```

---

### Slide 13 — Colab Step 2：下載模型說明

**標題：** Colab  
**內容：** 下載 checkpoint 和 LoRA，有提供範例的，也可自行去 civitai 上找尋自己想要的

**圖片 (slide13_img1.png)：** 「第二步：下載模型」：
- 如何下載任意模型和風格模型？
- 1. 一般情況模型放在 checkpoints 文件夾，風格模型放在 loras 文件夾
- 2. 需替換以下三個欄位：
  - **url**：這個文件的下載地址
  - **folder**：應存放的文件夾名字（模型→checkpoints，LoRA→loras）
  - **name**：文件名格式為 xxx.safetensors，xxx 只能使用英文、數字和下劃線；不同模型需要不同名字，否則會被覆蓋
  - 參考命名：sd35_large_fp8.safetensors、majic.safetensors、anylora.safetensors

---

### Slide 14 — Colab：下載 Checkpoint（based66_v30）

**標題：** Colab  
**內容：** 下載 checkpoint（Based66_V30）

**圖片 (slide14_img1.png)：** Colab 程式碼：
- 模型資訊：類型: sdxl（實際為 SD 1.5），文件大小: 1.99G
- 下載 URL：https://civitai.com/api/download/models/67841?type=Model&format=SafeTensor&size=pruned&fp=fp16

```python
url    = "https://civitai.com/api/download/models/67841?type=Model&format=SafeTensor&size=pruned&fp=fp16"
folder = "checkpoints"
name   = "based66_v30.safetensors"
download_from_civitai(url, folder, name)
```

---

### Slide 15 — Colab：下載 LoRA 及其他模型

**標題：** Colab  
**內容：** LoRA 同 checkpoint

**圖片 (slide15_img1.png)：** Colab 程式碼（完整可讀）：

**LoRA 模型：**
```python
# chibi-laugh LoRA
url    = "https://civitai.com/api/download/models/74646?type=Model&format=SafeTensor"
folder = "loras"
name   = "chibi-laugh.safetensors"
download_from_civitai(url, folder, name)

# boldline LoRA
url    = "https://civitai.com/api/download/models/86269?type=Model&format=SafeTensor"
folder = "loras"
name   = "boldline.safetensors"
download_from_civitai(url, folder, name)
```

**snapshot_download（HuggingFace 模型）：**
```python
from huggingface_hub import snapshot_download

# ControlNet 模型
repo_id   = 'comfyanonymous/ControlNet-v1-1_fp16_safetensors'  # 可替換成其他模型ID
cache_dir = '/content/ComfyUI/models/controlnet'               # 替換為你希望保存模型的路徑
snapshot_download(repo_id=repo_id, cache_dir=cache_dir)

# VAE 模型
repo_id   = 'stabilityai/sd-vae-ft-mse-original'  # 可替換成其他模型ID
cache_dir = '/content/ComfyUI/models/vae'          # 替換為你希望保存模型的路徑
snapshot_download(repo_id=repo_id, cache_dir=cache_dir)
```

> 注意：AnimateDiff motion adapter（motionModel.v01.ckpt / guoyww/animatediff-motion-adapter-v1-5-2）
> 由 ComfyUI Manager 中的 AnimateDiff 插件在安裝時自動下載，或需手動放置於
> `/content/ComfyUI/models/animatediff_models/`

---

### Slide 16 — Colab：啟動 ComfyUI

**標題：** Colab  
**內容：** 下載完後執行啟動 ComfyUI 網頁

**圖片 (slide16_img1.png)：** 「第三步：啟動 ComfyUI 網頁」

```python
!npm install -g localtunnel

import subprocess
import threading
import time
import socket
import urllib.request

def iframe_thread(port):
    while True:
        time.sleep(0.5)
        sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        result = sock.connect_ex(('127.0.0.1', port))
        if result == 0:
            break
        sock.close()

    print("\nComfyUI 載入，正在啟動 localtunnel...\n")
    try:
        req = urllib.request.Request('https://ipv4.icanhazip.com')
        ip = urllib.request.urlopen(req).read().decode('utf8').strip()
        print("=" * 50)
        print(f"請在網頁的「Endpoint IP」欄位中輸入這個密碼: {ip}")
        print("=" * 50 + "\n")
    except Exception as e:
        print("無法獲取 IP:", e)

    p = subprocess.Popen(["lt", "--port", str(port)], stdout=subprocess.PIPE)
    for line in p.stdout:
        print("ComfyUI 網址:", line.decode().strip())

threading.Thread(target=iframe_thread, daemon=True, args=(8188,)).start()

!python /content/ComfyUI/main.py --enable-manager --dont-print-server
```

---

### Slide 17 — Colab：確認執行階段

**標題：** Colab  
**內容：** 確認執行階段後點擊連結  
**標注：** 分配 IP

**圖片 (slide17_img1.png)：** Colab 輸出結果：
- 印出 Endpoint IP（即你的真實 IP）
- 印出 ComfyUI 網址（loca.lt 隧道 URL）
- 格式：`ComfyUI 網址: https://xxxx.loca.lt`

---

### Slide 18 — ComfyUI：輸入 IP 通過驗證

**標題：** ComfyUI  
**內容：** 輸入分配 IP 後點擊繼續

**圖片 (slide18_img1.png)：** localtunnel 驗證頁面：
- 瀏覽器頁面要求輸入 Endpoint IP 以確認身份
- 輸入後點選「Click to Submit」按鈕即可進入

---

### Slide 19 — ComfyUI：成功進入

**標題：** ComfyUI  
**內容：** 成功進入 ComfyUI

**圖片 (slide19_img1.png)：** 空白 ComfyUI 介面成功載入（無節點，新的空白工作流）

---

### Slide 20 — ComfyUI：下載工作流 JSON

**標題：** ComfyUI  
**內容：** 工作流下載

**圖片 (slide20_img1.png)：** Colab 左側檔案瀏覽器，顯示工作流 JSON 檔案位置，可從此下載

---

### Slide 21 — ComfyUI：匯入工作流

**標題：** ComfyUI  
**內容：** 匯入剛剛下載的工作流（.json）  
**標注：** 拖拉檔案至 ComfyUI

**圖片 (slide21_img1.png)：** ComfyUI 介面，左側顯示 Colab 檔案瀏覽器開啟，將 JSON 檔案拖曳至 ComfyUI 視窗即可載入工作流

---

### Slide 22 — ComfyUI：安裝遺失套件

**標題：** ComfyUI  
**標注：** 安裝遺失套件

**圖片 (slide22_img1.png)：** ComfyUI Manager（版本 v3.32.2）對話框，點選「Install Missing Custom Nodes」選項

---

### Slide 23 — ComfyUI：遺失套件清單

**標題：** ComfyUI  
**標注：** 安裝遺失套件後重新整理網頁

**圖片 (slide23_img1.png)：** ComfyUI Manager 顯示需安裝的套件：
- 「1 custom nodes」需安裝
- 套件名稱：**comfy-image-save**（Save Image with Generation Metadata）

---

### Slide 24 — ComfyUI：安裝後重新整理

**標題：** ComfyUI  
**標注：** 安裝遺失套件後重新整理網頁

**圖片 (slide24_img1.png)：** 安裝中或安裝後頁面顯示（部分節點仍顯示紅框，重新整理後消失）

---

### Slide 25 — ComfyUI：確認所有節點正常

**標題：** ComfyUI  
**內容：** 確認所有 nodes 皆無紅框

**圖片 (slide25_img1.png)：** 完整工作流縮小視圖，所有節點連接正確、無紅框錯誤，共 23 個節點

---

### Slide 26 — ComfyUI：設定 Seed Generator

**標題：** ComfyUI  
**標注：** 更改種子生成器為 randomize

**圖片 (slide26_img1.png)：** Seed Generator 節點，下拉選單已從「fixed」改為「**randomize**」（每次生成使用不同隨機種子）

---

### Slide 27 — ComfyUI：編輯提示詞

**標題：** ComfyUI  
**內容：** 
- 請更換成自己的提示詞
- 提示詞模板請參考下面的備忘稿

**圖片 (slide27_img1.png)：** Batch Prompt Schedule 節點，顯示時間軸提示詞輸入框（依幀數分配不同描述）

**備忘稿（Speaker Notes）— Sample 1 提示詞模板：**
```
"0"  : "spring day, floral skirt, wind, hair accessories, smile",
"10" : "spring day, floral skirt, wind, hair accessories, smile",
"20" : "spring day, floral skirt, wind, hair accessories, smile",
"30" : "summer day, short-sleeved dress, straw hat",
"40" : "summer day, short-sleeved dress, straw hat",
"50" : "summer day, short-sleeved dress, straw hat",
"60" : "fall day, sweater, slim jeans, wind, fallen leaves",
"70" : "fall day, sweater, slim jeans, wind, fallen leaves",
"80" : "fall day, sweater, slim jeans, wind, fallen leaves",
"90" : "winter, down jacket, woolen hat, ear protection gloves, snowflakes",
"100": "winter, down jacket, woolen hat, ear protection gloves, snowflakes",
"110": "winter, down jacket, woolen hat, ear protection gloves, snowflakes"
```

---

### Slide 28 — ComfyUI：開始生成

**標題：** ComfyUI  
**標注：** 按下運行開始生成影片

**圖片 (slide28_img1.png)：** ComfyUI 工作流，兩個 Video Combine 節點以橙色邊框高亮顯示（表示為輸出節點），點按「Queue Prompt」開始執行

---

### Slide 29 — Colab：下載輸出檔案

**標題：** Colab  
**標注（多個）：**
- 生成完畢後，回到 Colab 找到生成的影片
- 生成影片（AnimateDiff_00001.mp4）
- 生成圖片（AnimateDiff_00001.png）
- 生成圖片（GIF_00001.png）
- 下載這兩個檔案放在作業網頁

**圖片 1 (slide29_img1.png)：** Colab 左側檔案瀏覽器

**圖片 2 (slide29_img2.png)：** 輸出資料夾內容，包含以下生成檔案：
- `AnimateDiff_00001.mp4`（影片檔）
- `AnimateDiff_00001.png`（影片縮圖）
- `GIF_00001.gif`（GIF 動畫）
- `GIF_00001.png`（GIF 縮圖）

---

### Slide 30 — ComfyUI：手動觸發 Video Combine

**標題：** ComfyUI  
**內容：** 如果生成結束後，沒有在 colab 資料夾裝的 output 出現成品，請按下兩個 Video Combine 的執行鍵

**圖片 1 (slide30_img1.png)：** ComfyUI 工作流，橙色高亮標示兩個 Video Combine 節點

**圖片 2 (slide30_img2.png)：** ComfyUI 完整視圖細節：
- 標注：「執行至選取的輸出節點（以橙色邊框標示）」
- **Video Combine 1（MP4）：**
  - frame_rate: 8、loop_count: 0
  - filename_prefix: AnimateDiff
  - format: video/h264-mp4、pix_fmt: yuv420p、crf: 20
  - save_metadata: true、trim_to_audio: false、pingpong: false、save_output: true
- **Video Combine 2（GIF）：**
  - frame_rate: 1、loop_count: 0
  - filename_prefix: GIF
  - format: image/gif
  - pingpong: false、save_output: true
- 右側預覽圖片：動漫男性角色站在海灘上（深色外套）

---

### Slide 31 — Sample 1：四季換裝（春夏秋冬）

**標題：** Sample

**GIF (slide31_img1.gif) 第一幀（春）：** 動漫少女，淺棕/金色頭髮，雙馬尾小圓髮包，藍色長袖短版上衣，粉色碎花裙，手提藤編籃子，站在花園小徑（春天，笑容燦爛）

**提示詞（Batch Prompt Schedule）：**
```
"0"  : "spring day, floral skirt, wind, hair accessories, smile",
"10" : "spring day, floral skirt, wind, hair accessories, smile",
"20" : "spring day, floral skirt, wind, hair accessories, smile",
"30" : "summer day, short-sleeved dress, straw hat",
"40" : "summer day, short-sleeved dress, straw hat",
"50" : "summer day, short-sleeved dress, straw hat",
"60" : "fall day, sweater, slim jeans, wind, fallen leaves",
"70" : "fall day, sweater, slim jeans, wind, fallen leaves",
"80" : "fall day, sweater, slim jeans, wind, fallen leaves",
"90" : "winter, down jacket, woolen hat, ear protection gloves, snowflakes",
"100": "winter, down jacket, woolen hat, ear protection gloves, snowflakes",
"110": "winter, down jacket, woolen hat, ear protection gloves, snowflakes"
```

---

### Slide 32 — Sample 2：海灘帥哥（晨昏四景）

**標題：** Sample

**GIF (slide32_img1.gif) 第一幀（早晨）：** 動漫男性，深棕短髮，黑色轟炸機外套，米色貨運長褲，黑色軍靴，站在沙灘海邊（清晨）

**提示詞（Batch Prompt Schedule）：**
```
"0"  : "1boy, handsome, short hair, workwear jacket, cargo pants, morning beach, ocean waves, clear sky, walking",
"10" : "1boy, handsome, short hair, workwear jacket, cargo pants, morning beach, ocean waves, clear sky, walking",
"20" : "1boy, handsome, short hair, workwear jacket, cargo pants, morning beach, ocean waves, clear sky, walking",
"30" : "1boy, handsome, short hair, workwear vest, white t-shirt, cargo shorts, sunny beach, ocean, blue sky, wearing sunglasses",
"40" : "1boy, handsome, short hair, workwear vest, white t-shirt, cargo shorts, sunny beach, ocean, blue sky, wearing sunglasses",
"50" : "1boy, handsome, short hair, workwear vest, white t-shirt, cargo shorts, sunny beach, ocean, blue sky, wearing sunglasses",
"60" : "1boy, handsome, short hair, unbuttoned workwear shirt, cargo pants, sunset beach, golden hour, wind, dramatic lighting",
"70" : "1boy, handsome, short hair, unbuttoned workwear shirt, cargo pants, sunset beach, golden hour, wind, dramatic lighting",
"80" : "1boy, handsome, short hair, unbuttoned workwear shirt, cargo pants, sunset beach, golden hour, wind, dramatic lighting",
"90" : "1boy, handsome, short hair, dark workwear jacket, cargo pants, night beach, starry sky, moonlight, ocean reflections",
"100": "1boy, handsome, short hair, dark workwear jacket, cargo pants, night beach, starry sky, moonlight, ocean reflections",
"110": "1boy, handsome, short hair, dark workwear jacket, cargo pants, night beach, starry sky, moonlight, ocean reflections"
```

---

### Slide 33 — Sample 3：黑髮少女（海灘四景）

**標題：** Sample

**GIF (slide33_img1.gif) 第一幀（早晨）：** 動漫少女，黑色長直髮馬尾，白色無袖棉麻洋裝（肩帶款），赤腳，走在沙灘上（側後身視角）

**提示詞（Batch Prompt Schedule）：**
```
"0"  : "1girl, black hair, ponytail, opaque white cotton sundress, modest, morning beach, clear sky, soft morning light, ocean waves, walking",
"10" : "1girl, black hair, ponytail, opaque white cotton sundress, modest, morning beach, clear sky, soft morning light, ocean waves, walking",
"20" : "1girl, black hair, ponytail, opaque white cotton sundress, modest, morning beach, clear sky, soft morning light, ocean waves, walking",
"30" : "1girl, black hair, ponytail, opaque white cotton sundress, modest, sunny beach, noon, bright sunlight, clear blue sky, sparkling water",
"40" : "1girl, black hair, ponytail, opaque white cotton sundress, modest, sunny beach, noon, bright sunlight, clear blue sky, sparkling water",
"50" : "1girl, black hair, ponytail, opaque white cotton sundress, modest, sunny beach, noon, bright sunlight, clear blue sky, sparkling water",
"60" : "1girl, black hair, ponytail, opaque white cotton sundress, modest, sunset beach, golden hour, warm lighting, dramatic sky, ocean breeze",
"70" : "1girl, black hair, ponytail, opaque white cotton sundress, modest, sunset beach, golden hour, warm lighting, dramatic sky, ocean breeze",
"80" : "1girl, black hair, ponytail, opaque white cotton sundress, modest, sunset beach, golden hour, warm lighting, dramatic sky, ocean breeze",
"90" : "1girl, black hair, ponytail, opaque white cotton sundress, modest, night beach, starry sky, moonlight, dark ocean, glowing reflections",
"100": "1girl, black hair, ponytail, opaque white cotton sundress, modest, night beach, starry sky, moonlight, dark ocean, glowing reflections",
"110": "1girl, black hair, ponytail, opaque white cotton sundress, modest, night beach, starry sky, moonlight, dark ocean, glowing reflections"
```

**Negative Prompt：** `(bad quality, worst quality:1.2), sheer, transparent, translucent, revealing, wet clothes`

---

### Slide 34 — 章節分隔：避免 Colab 閒置
章節 03

---

### Slide 35 — 如何避免斷線

**標題：** 如何避免斷線  
**標注：** 貼在這裡

**步驟：**
1. 執行 Colab 中的整段程式碼
2. 看到畫面上印出 Endpoint IP 和 ComfyUI 網址
3. 在 Colab 的網頁按下鍵盤的 F12，切換到 Console 頁籤
4. 複製並貼上防斷線腳本（下一張投影片），按 Enter 執行

**圖片 (slide35_img1.png)：** 瀏覽器 DevTools — Console 頁籤已開啟，命令列輸入框（>）可見

---

### Slide 36 — 防斷線腳本

**標題：** 防斷線腳本  
**說明：** 這段 JavaScript 的程式碼，會自動每 60 秒刷新 Colab 網頁，為了避免 ComfyUI 網頁跑太久，而被 Colab 判定為閒置

```javascript
function ClickConnect(){
  console.log("正在點擊連線按鈕以防斷線...");
  const colabConnectButton = document.querySelector("#top-toolbar colab-connect-button");
  if (colabConnectButton) colabConnectButton.click();
}
setInterval(ClickConnect, 60000); // 60秒(60000毫秒)點擊一次
```

---

### Slide 37 — 跳出瀏覽器安全警告

**標題：** 跳出瀏覽器安全警告

**內容：** 若出現警告（如圖所示）：
- 此警告是為了保護使用者的安全防護機制，會擋直接貼上的輸入
- 請在要貼程式碼的位置 `>` 的後面輸入：`allow pasting`，並按下 Enter
- 將防斷線腳本再次貼上

**圖片 (slide37_img1.png)：** 瀏覽器安全警告畫面，DevTools Console 提示禁止直接貼上

---

### Slide 38 — 成功畫面

**標題：** 成功畫面

**內容：**
- 成功貼上後會跳出：`14936`（計時器的 ID）
- 60 秒後會跳出：`正在點擊連線按鈕以防斷線...`
- 每 60 秒，前面的數字會 +1

**圖片 (slide38_img1.png)：** Console 顯示：計時器 ID 號碼 + 防斷線訊息成功輸出

---

### Slide 39 — 章節分隔：繳交資訊
章節 04

---

### Slide 40 — Regulations

> You should finish your homework on your own.  
> Do not share your codes with any living creatures.  
> Your HW will get 0 pt if you violate any of the above rules.  
> Professor & TAs preserve the rights to change the rules & grades.

---

### Slide 41 — 章節分隔：助教聯絡資訊
章節 05

---

### Slide 42 — 助教聯絡資訊

| 項目 | 內容 |
|------|------|
| TA | 賴秋彤 |
| TA Email | t114598033@ntut.org.tw |
| Email 主旨格式 | [ai2026s-hwX-學號] |

---
---

## 教授 HW06 解答範例 (https://lctung.github.io/ai2026s/hw06/index.html)

---

### 評分表（滿分 10/10）

| 難度 | 完成狀況 |
|------|---------|
| Simple | 完成 ✅ |
| Medium | 完成 ✅ |
| Strong | 完成 ✅ |
| 心得 | 完成 ✅ |

---

### 心得（Essay）

> 本次作業是接觸文生影片的初步應用，使用的是目前提供個人使用功能最齊全的文生圖工具 ComfyUI，以及使用在 Civitai 上開源的模型，透過節點式的方式連接模塊，構建工作流並執行產生影片，過程有趣且也能透過該過程理解模型運作流程，最後成功生成影像。

---

### Simple Baseline（綠色區塊）

**環境資訊：**
- CheckPoint：**based66_v30**
- LoRA：**chibi-laugh**

**ComfyUI 工作流截圖（完整 AnimateDiff 文生影片工作流）：**

工作流名稱：「文生影片」（分頁標題）  
節點數量：N:23[23]，V:51  
狀態：Job completed

節點列表（從左到右、上到下）：

| 節點名稱 | 設定值 |
|---------|--------|
| 載入檢查點 | based66_v30.safetensors |
| LoRA Loader（×2） | chibi-laugh / boldline |
| Empty Latent Image Big Batch | 寬 512 × 高 768，batch=8 |
| AnimateDiff Loader Legacy [DEPR] | motionModel.v01.ckpt，sqrl_linear schedule |
| AnimateDiff-Evolved [DEPR] | AnimateDiff 主調度器 |
| Batch Prompt Schedule Latent Input [FizzNodes] | context_length=16，context_stride=1，context_overlap=4，start_frame=0，end_frame=10 |
| KSampler (Advanced) | steps=20，cfg=8.0，sampler=euler |
| 載入VAE | vae-ft-mse-840000-ema-pruned.safetensors |
| VAE 解碼 | — |
| Seed Generator | 模式：randomize |
| VideoHelperSuite | — |
| Video Combine 1 | format: video/h264-mp4，filename_prefix: AnimateDiff，frame_rate: 8，crf: 20，save_metadata: true，pingpong: false，save_output: true |
| Video Combine 2 | format: image/gif，filename_prefix: GIF，frame_rate: 1，save_output: true |
| comfy-image-save | 帶 metadata 儲存節點 |

---

### Medium Baseline（紅色區塊）— 生成角色的圖片 1、2、3

共 3 張靜態角色圖片（從動畫工作流生成的靜態幀）：

- **圖片 1**：動漫少女，淺棕色頭髮雙馬尾，藍色上衣，粉色碎花裙，藤編籃子，在花園小徑（春季場景）
- **圖片 2**：動漫少女，黑色馬尾，白色無袖洋裝，在海邊（海灘場景，與 Sample 3 同角色）
- **圖片 3**：動漫男性，深色外套，貨運褲，軍靴，在海灘（與 Sample 2 同角色）

（三張圖片均為角色主體全身或下半身構圖）

---

### Strong Baseline（紫色區塊）— 生成完整角色動畫 1、2、3

三個 GIF 動畫，對應講義 Sample 1、2、3（教授的範例即為課堂示範樣本）：

**動畫 1（四季換裝）：**
- 角色：淺棕色頭髮少女（藍色上衣 + 粉碎花裙，花園小徑）
- 內容：春→夏→秋→冬 服裝切換
- 提示詞：同 Slide 31 Sample 1

**動畫 2（海灘帥哥 晨昏四景）：**
- 角色：深棕短髮男性（黑外套 + 貨運褲 + 軍靴，海灘）
- 內容：清晨→正午→黃昏→夜晚 光線與服裝切換
- 提示詞：同 Slide 32 Sample 2

**動畫 3（黑髮少女 海灘四景）：**
- 角色：黑色馬尾少女（白色棉麻洋裝，赤腳，海灘）
- 內容：清晨→正午→黃昏→夜晚 光線切換
- 提示詞：同 Slide 33 Sample 3
- Negative Prompt：`(bad quality, worst quality:1.2), sheer, transparent, translucent, revealing, wet clothes`

---
---

## 快速參考：HW06 所需檔案與指令

### 模型下載指令

```python
# Checkpoint
url    = "https://civitai.com/api/download/models/67841?type=Model&format=SafeTensor&size=pruned&fp=fp16"
folder = "checkpoints"
name   = "based66_v30.safetensors"
download_from_civitai(url, folder, name)

# LoRA 1: chibi-laugh
url    = "https://civitai.com/api/download/models/74646?type=Model&format=SafeTensor"
folder = "loras"
name   = "chibi-laugh.safetensors"
download_from_civitai(url, folder, name)

# LoRA 2: boldline
url    = "https://civitai.com/api/download/models/86269?type=Model&format=SafeTensor"
folder = "loras"
name   = "boldline.safetensors"
download_from_civitai(url, folder, name)

# VAE
from huggingface_hub import snapshot_download
repo_id   = 'stabilityai/sd-vae-ft-mse-original'
cache_dir = '/content/ComfyUI/models/vae'
snapshot_download(repo_id=repo_id, cache_dir=cache_dir)
```

### 工作流設定重點

| 設定項目 | 值 |
|---------|-----|
| Seed Generator | randomize |
| Image size | 512 × 768 |
| Batch size | 8 |
| KSampler steps | 20 |
| KSampler cfg | 8.0 |
| KSampler sampler | euler |
| AnimateDiff motion model | motionModel.v01.ckpt |
| context_length | 16 |
| Video frame_rate (MP4) | 8 fps |
| Video frame_rate (GIF) | 1 fps |
| MP4 crf | 20 |

### 防斷線腳本

```javascript
function ClickConnect(){
  console.log("正在點擊連線按鈕以防斷線...");
  const colabConnectButton = document.querySelector("#top-toolbar colab-connect-button");
  if (colabConnectButton) colabConnectButton.click();
}
setInterval(ClickConnect, 60000);
```
在 Colab 網頁按 F12 → Console → 若出現安全警告先輸入 `allow pasting` Enter → 再貼腳本

### 輸出檔案（需上傳至 hw06/index.html）

| 檔案 | 用途 |
|------|------|
| `AnimateDiff_00001.mp4` | Strong Baseline 影片（MP4） |
| `GIF_00001.gif` | Strong Baseline 動畫（GIF） |
| （截圖）ComfyUI 環境畫面 | Simple Baseline 截圖 |
| （截圖）生成的靜態圖片 3 張 | Medium Baseline |

### 繳交資訊

- GitHub Pages URL：`https://svw2404.github.io/ai2026s/hw06/index.html`
- TA Email：t114598033@ntut.org.tw
- Email 主旨：[ai2026s-hw6-學號]
- 遲交：分數打五折
