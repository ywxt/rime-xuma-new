# 新徐碼輸入方案

本方案爲採用**繁體簡碼**的*新版*徐碼輸入方案，方案設計來自[rime-xuma](https://github.com/Ace-Who/rime-xuma)，碼表來自[forFudan/xuma](https://github.com/forFudan/xuma)的調整版方案。

**⛔⛔⛔: 由於上游刪除了`Less Z` 方案，所以此項目不再更新。如有需要，請使用其他方案。**

## 使用必看

1. **此方案爲新版徐碼（2022），非舊版徐碼**。新版徐碼字根經過了一定的調整，新舊徐碼並不相同，使用之前先看清楚。
2. **此方案碼表是[Less Z/forFudan調整版](https://github.com/forFudan/xuma)**。此方案非官方版，而是在新徐碼的基礎上調整了部分字根分佈，減少 `Z` 和`X` 鍵上的字根數量，調整小碼爲 `z` 或 `x` 的字根，優化手感。因爲官方版本在 `Z` 和 `X` 上安排了太多的字根，導致倚重小指。
   Less Z/forFudan 調整版具體說明參見原項目 README 。

## 使用介紹

- 字集選擇：
  
  - 常用： 常用國字標準字字體表 + 次常用國字標準字字體表 + 第一批異體整理表（GBK部分） + 部分大陸香港字形（例：爲、衆等字）。此字集並不包含日本新字體。共近12000個漢字。
  
  - 全集： 不過濾字集

- 反查： ``` ` ```（反引號）反查，``` `P ```拼音反查，``` `B ``` 五筆畫反查。

- 全碼後置： 簡碼單字排序靠前，全碼重碼時降低排序，讓位於無簡碼字詞。默認開啓。

- 手動造詞： 使用``` ` ```（反引號）分割單字編碼，如：``` xx`xx`xx ```

- 選重： `；`（分號）次選，`'`（引號）三選。

- 繁入簡出：快捷鍵 `Ctrl + Shift + Space` ，默認關閉。

- 外文過濾：只保留漢字/不過濾，默認關閉。

- 字根分佈圖：*此方案簡碼設置與字根圖不同，使用時請注意*。
   ![字根分佈圖](https://github.com/forFudan/xuma/blob/main/resources/%E5%BE%90%E7%A2%BC%E5%AD%97%E6%A0%B9%E9%8D%B5%E4%BD%8D%E5%9C%96ForFudan%E8%AA%BF%E6%95%B4.jpg?raw=true)
  
## 使用方案

複製目錄下所有文件到用戶文件夾，然後重新部署。

**注：如果你已有`rime.lua`文件，不要直接替換，而是把本方案的`rime.lua`文件的內容追加到你的`rime.lua`中。**

**注： 確保你已經有朙月拼音和五筆劃方案，否則不能部署成功。**

## Q&A

1. Q： 爲什麼部署不成功？

   A： 確保你已經有朙月拼音和五筆劃方案，部分發行版（例如同文輸入法）並不內置，需要手動下載。 [朙月拼音](https://github.com/rime/rime-luna-pinyin) [五筆畫](https://github.com/rime/rime-stroke)

2. Q： 爲什麼部分功能無法使用（如字集過濾）？

   A： 確保你的發行版支持lua插件。

3. Q： 如何刪除用戶自造詞？

   A:  
      > 删除特定用户词：输入该词编码，移动光标选中该词，敲删词键 Ctrl + Delete 或 Shift + Delete （Mac OS 用 Shift + Fn + Delete），默认还绑定了 Ctrl + K。删除整个用户词典：先退出输入法程序或算法服务， 然后删除用户目录下的 xuma-new.userdb 目录，再启动输入法。

4. Q: 與[forFudan/xuma](https://github.com/forFudan/xuma)碼表不同之處

   A:
      - 去除大部分字根字的特碼，比如 `訁(Yvv)` ，恢復爲 `Yv` 。但是保留部分與高頻字衝突的特碼。詳見末表。
      - 去除碼表中的符號，如需使用，可以通過符號方式輸入（如`/jg`）。
      - 不包含康熙部首，因爲這部分目前未更新編碼。
      - 不包含拆分提示。
  
### 保留的特碼

```plain
乃 ann
爿 app
糸 avv
飛 bff
艮 bgg
乙 bii
予 byy
巴 dbb
弓 dgg
刀 dhh
皮 dpp
尸 dvv
韋 dww
丁 edd
甫 ejj
馬 emm
酉 eoo
臣 fee
戈 fgg
弋 fii
戊 fjj
牙 fyy
歹 gdd
辰 gnn
豕 gss
石 gvv
兀 gww
頁 gyy
甘 hee
革 hgg
耳 hrr
寸 icc
丰 iff
木 ivv
爾 jee
古 jgg
尤 joo
犬 jqq
土 jvv
雨 jyy
甲 kjj
曰 kuu
由 kyy
鹵 lll
虫 lvv
巾 mjj
冊 muu
貝 nbb
鬥 ndd
骨 ngg
門 nmm
呂 ouu
矢 pii
血 pmm
牛 pnn
几 qjj
欠 qqq
爪 raa
九 rjj
舟 roo
壬 rrr
禾 rvv
夭 ryy
鼻 tbb
自 tii
片 tpp
八 tuu
鬼 ugg
臼 ujj
僉 uqq
烏 uww
豸 vcc
穴 wee
鹿 wll
麻 woo
衣 wyy
火 xvv
亥 yhh
亦 yii
辛 yss
申 ksss
```
