# InDesign 排字調整設定（标点挤压设置、文字組みセット）

## 載入設定

根目錄下後綴為 `.idml` （IDML，InDesign Markup Language）的文件包含了所有調整設定。下載後，在「排字調整設定[^doc]」讀入所需文件，接下來的面板中啟動「所有文件」便能以 IDML 的格式導入（默認僅允 `.indd`〔InDesign Document〕）。

## 設定集

- 居中標點直書（[`TategakiCP.idml`](https://github.com/toto-minai/MojikumiTable/raw/main/TategakiCP.idml)）

## 說明

各文件夾的內容為 IDML 文件解壓縮後的狀態。其中，`designmap.xml` 的 `<MojikumiTable>` 區段包含一套排字調整設定。請編寫各 `<OverrideMojikumiAkiType>` 條目調整字元間額外空隙大小的極值和理想值。字形與序號的關係[列表如下](#字形對照表)。

任意目錄下，可以使用命令行工具進行壓縮，最終製成可讀入的 IDML 文件（更多製作方式請參考[官方手冊](https://wwwimages.adobe.com/content/dam/acom/en/devnet/indesign/sdk/cs6/idml/idml-cookbook.pdf)）：

```bash
zip -r "../$(basename $PWD).idml" .
```

## 字形對照表

| 序號[^index] | InDesign 名稱 | 例 |
|-|-|-|
| 1  | 其他左括號 | |
| 2  | 其他右括號 | |
| 3  | 頂端避頭尾 | |
| 4  | 結束標點符號 | ！？ |
| 5  | 音界號 | ・ |
| 6  | 日文句點 | 。 |
| 7  | 連續符號 | ―⋯… |
| 8  | 數字之前 | ￥＄ |
| 9  | 數字之後 | ％℃ |
| 10 | 全形空格 | |
| 11 | 平假名 | |
| 12 | 中文 | |
| 18 | 羅馬字 | |
| 21 | 中文頓號 | 、 |
| 22 | 行首符號 | |
| 23 | 段落符號 | |
| 24 | 全形數字 | |
| 25 | 半形數字 | |
| 26 | 尖形左括號 | 「『 |
| 27 | 圓形左括號 | （ |
| 28 | 尖形右括號 | 」』 |
| 29 | 圓形右括號 | ） |
| 30 | 逗號 | ， |
| 31 | 英文句點 | ． |
| 32 | 冒號 | ：； |
| 33 | 片假名 | |

[^doc]: 具體設定請訪問[官方文檔](https://helpx.adobe.com/hk_zh/indesign/using/composing-cjk-characters.html)。
[^index]: 即 `TargetMojikumiClass` 或 `SideMojikumiClass` 的數值。