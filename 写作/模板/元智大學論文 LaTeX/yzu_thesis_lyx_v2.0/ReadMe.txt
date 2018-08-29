(this text file is encoded in UTF8)
v2.0 (Apr. 5, 2009)
** 包含了哪些檔？

這個「論文格式檔」其實包含了不只一個檔案，有下列 19 個檔案，再加上此篇 ReadMe.txt 文字檔：
my_ackn.tex
my_appendix.lyx
my_bib.bib
my_cabstract.tex
my_eabstract.tex
my_headerfooter.tex
my_names.tex
my_symbols.tex
my_vita.tex
my_watermark.jpg
my_watermark.bb
yzu_backpages.lyx
yzu_chnum.tex
yzu_definitions.tex
yzu_frontpages.tex
yzu_report.cls
yzu_report.layout
yzu_thesis.lyx
yzu_watermark.tex

以上這些檔案請勿更改檔名。
副檔名檔名是 .lyx 者，用 LyX 應用程式編輯；副檔名是 .tex 者，用一般 LaTeX 文稿編輯器編輯。

以 yzu_ 為首的幾個檔案，除了 yzu_thesis.lyx 以外，其餘內容不需因人修改，除非校方的格式有所變動。
以 my_ 為首的幾個檔案內容則一定要依個人的情況加以修改撰寫：
	my_ackn.tex 的內容會出現在「誌謝」頁裡，不必含標題；
	my_appendix.lyx 的內容會出現在「附錄」；如有多個附錄請都在此檔內繕寫，並以所附的編排碼作為每個附錄的起頭；
	my_bib.bib 是參考文獻的 BibTeX 資料庫。所有會引用到的文獻都請放入此檔；格式可以參考所附的範例，或以另外的工具程式管理，如 EndNote、BibDesk (免費，Mac OS X)、JabRef (Java, 跨平台 MS Windows, Mac OS X, Linux)；
	my_cabstract.tex 的內容會出現在「中文摘要」頁裡的摘要內容，不必含其他標題、姓名等制式格式；
	my_eabstract.tex 的內容會出現在「英文摘要」頁裡的摘要內容，不必含其他標題、姓名等制式格式；
	my_headerfooter.tex 如果校方格式要求頁楣 (header)(如，章名戳記)以及頁碼以外的 footer (如日期)，則請在此檔內依所附範例 (檔內之註解) 修改。因為元智大學無此規定，所以檔內內容是以註解符號關閉的。
	my_names.tex 裡定義了你的姓名、論文題目、指導教授姓名、系所名、學位名等個人資料；
	my_symbols.tex 的內容會出現在「符號說明」頁；請依所附範例格式繕寫；
	my_vita.tex 的內容會出現在「自傳」頁裡，不必含標題；
	my_watermark.jpg  如果校方規定需要在內文裡加上浮水印，則請將所需的圖檔命名為 my_watermark，副檔名則不一定非得是 .jpg 不可，視圖檔格式而定，程式會自動取得；
	my_watermark.bb  前述浮水印圖檔的 boundary box 定義檔；由系統的工具程式 ebb 產生；只有在 latex+divpdfmx 工作流程時，對於非 .eps 的圖檔才需要；所附的此檔只能配合所附的元智浮水印圖檔；詳情請看下面關於「工作流程」的介紹。

至於以 example_ 為首的幾個檔案，則是用來做示範用的，看完後可以丟棄:
	example_body.lyx  示範論文的章節內容
	example_fig.png  示範論文所用的圖檔 (彩色元智校徽)
	example_prog_list.m  示範論文所用的 MATLAB 的程式列表用的文字檔
	example_thesis.pdf  所產生的論文 pdf, 檔名已經從 yzu_thesis.pdf 改為 example_thesis.pdf，以防止再編譯 example 時被覆寫。
	example_coverbridge.pdf 是由獨立的 yzu_coverbridge.tex 所產生的論文書背列印檔。檔名已經從 yzu_coverbridge.pdf 改為 example_coverbridge.pdf，以防止再編譯時被覆寫。必須由 LaTeX 直接排版，而不是使用 LyX。

	




** 安裝格式檔 yzu_report.cls

在 TeXLive 所安裝的 LaTeX 系統，不必把 yzu_report.cls 裝到某個 [texmf] 地方，只要與所有這些格式檔放在一起即可。

如果不是 TeXLive 所安裝的，在使用格式檔寫論文之前，須先把 yzu_report.cls 裝在你的 LaTeX 系統裡。這些個人裝設的額外檔案，一般是放在 [texmf]/tex/latex/ 這裡。
(這裡，[texmf] 代表你的 TeX 系統的 texmf 檔案路徑。以 Mac OS X 裡 Gerben Wierda 的 teTeX 系統為例，個人可以動用的 [texmf] 是 
/usr/local/teTeX/share/texmf.local/ 
以及 
~/Library/texmf/ 
後者有較高的優先次序，但無法與系統裡的其他使用者共用)
裝好後，請記得在終端機程式裡執行 sudo texhash 來更新 tex 的紀錄。


** 安裝格式檔 yzu_report.layout

Mac 平台：
把它複製到
 ~/Library/Application Support/LyX-1.6/lauouts/
這個檔案夾裏。(版本號碼也許不一樣)

Windows 平台：
把它複製到
 C:\Program Files\lyx\lauouts\  ???
這個檔案夾裏。

複製後，啟動 LyX，執行 Reconfigure 選單命令。結束並再啟動 LyX。


** 使用方式

yzu_thesis.lyx 是主檔，其他檔案會自動被載入。
中文字體名稱在各系統裡的命名方式可能會不同，請更改 yzu_thesis.lyx 檔案設定。更改方法如下：
Document > Settings > Fonts > CJK
bsmi 改成適當的字體名稱，如「bkai」、「cwkai」。

建議全文分割成每章一個 lyx 檔。然後依 yzu_thesis.lyx 內之註解說明，在適當處以選單命令
Insert > File > Child document ... > Input (輸入)
條列各輸入之檔名。
各章之 lyx 檔可以由新建一個檔，然後在 
Document > Settings > Document Class ...
選擇與主檔相同之 yzu_report 格式即可，並在檔案最後一行加入文獻資料庫的隱藏資料。如 example_body.lyx 所示。

如此安排的好處是可以把其他已經寫好的暫時關掉，以省掉不必要的排版編譯時間。要把某章關掉，可以把該章所對應的 Input 方塊，以鼠標圈選後，以 Insert > Note > Comment 的方式變成註解。要把某章恢復，則以滑鼠右鍵在 Comment 上跳出的選單選擇 Dissolve inset。



** 元智大學的論文格式

關於元智大學的論文格式，可以在「元智教務處 > 學生專區 > 畢業/離校 > 學位論文格式規範」這網頁找到
<http://www.yzu.edu.tw/admin/aa/>
另有新的相關規定 (4/2006)，在「元智大學電子學位論文服務」網頁這裡
<http://etds.yzu.edu.tw/main/index>
是關於「電子檔規格說明」、「電子檔轉檔說明」、「電子檔上傳說明」。


** 浮水印

元智大學論文格式規範指定從書名頁開始要加上浮水印 (4/2006 新規範)；不過，其他有些學校沒有浮水印的要求，於是此一功能是可以關掉的 (在 yzu_thesis.lyx 的檔案設定，
Document > Settings > LaTeX Preamble 裏
把 \input{yzu_watermark.tex} 這行以百分號關掉即可)。

此一功能是借用加強型 header、footer 的套件 fancyhdr，佔用其中間 header 來擺放浮水印。在預設的情況下，是全篇加浮水印 (除封面以外)。如果要在單一頁加入浮水印，則在 yzu_watermark.tex 裡把全篇浮水印的程式碼關掉後 (詳見下一段)，依欲加浮水印該頁屬性，在該頁處使用下列之一的命令:
* 普通頁命令 (保留原頁面的 header、footer 設定): \thispagestyle{WaterMarkPage}
* plain 頁命令 (只保留 footer 頁碼，適合「章」層級的第一頁，以及「摘要」、目錄、參考文獻): \thispagestyle{PlainWaterMarkPage}
* empty 頁命令 (沒有頁碼，適合封面與書名頁): \thispagestyle{EmptyWaterMarkPage}

如果要關掉全篇加浮水印的功能，但保留少數頁自行加浮水印之功能，則請在 yzu_watermark.tex 這個檔案裡，把
%% >>> 全篇浮水印
%% <<< 全篇浮水印
之間的程式行首加上百分號，就可以了。

如果要加的是其他學校的浮水印，只要把校方提供的浮水印圖檔，改名為 my_watermark.xxx，這裡副檔名 .xxx 視實際圖檔格式而定，有可能是 .eps，.jpg，.png，.pdf 等各種 latex 或 pdftex 認得懂的格式。視你的工作流程 (pdftex 或 latex+dvipdfmx)，有可能需對此圖檔做前置作業。請參考下面的解釋。目前設定是在版面中間以寬度為 5.1 cm 加上浮水印的圖。


** 該用 pdflatex 還是 latex+dvipdfmx?

該用 pdflatex 還是 latex+dvipdfmx? 後者在內嵌字型時，使用較新的技術 (CID)，所以產生的 pdf 檔案較小，而且裡面的中文是可以拷貝出來、檢索的；不過，它在第一階段由 latex 編譯時，縱然由插圖套件 graphicx 加持，仍會遭遇到不識較近代的圖檔格式的圖的尺寸問題，如 jpg, png, pdf 等格式，必須先由一個叫 ebb 的小工具程式，在終端機程式裡先替這些圖檔程式產生 boundary box 的 .bb 檔案。至於 pdflatex，不會做 CID 的中文內嵌，而是用傳統的 subfont 的方式，但是也可以拷貝、檢索裡面的中文 (CJK 4.7.0版本之後即可)，不過，上述的圖檔則不需用 ebb 做前置處理，直接搞定，但反而對於較傳統的 .eps 檔需要先轉檔成 .pdf 或 .mps 的格式。
請參考這個網頁
<http://www.2pi.info/latex/Includingeps.html>

在編寫如論文這樣的大型文件，用 latex+dvipdfmx 會較有效率。如前面所述，要取得完整正確的內文交互參考編號與文獻編號，要編譯好幾次。pdflatex 每次編譯都要花時間從字型檔取得字型資料嵌入產生的 pdf 檔中，前幾次編譯時，這些嵌入字型資料的動作都是浪費時間；相反的，latex+dvipdfmx 只有在最後一步驟 dvipdfmx 才會做嵌入字型資料的動作，省了不少時間。


** 其他 header, footer 的範例

其他學校有 header、footer 的不同要求 (例如加有「章」戳記、有畫分隔線的 header，加有「日期」的 footer)，可以用 fancyhdr 套件的現有功能，在 my_headerfooter.tex 裡加以定義。目前在 my_headerfooter.tex 檔案裡，列有範例，可以參考定義的方式。不過，因為浮水印會佔用中間的 header，所以只能用左、右 header。


** 封面所需的書背

獨立的書背列印檔 yzu_coverbridge.tex，直接由 my_names.tex 的資料合成出所需的書背，方便印刷店家製作書背。遵循元智大學論文格式的附件 18。此檔與 yzu_thesis.lyx 無關。要使用時，直接以 pdflatex 或 latex + dvipdfmx 編譯此檔即可，不需修改任何地方。使用了 LaTeX CJK 的中文直排的功能。如果使用 latex + dvipdfmx 工作流程，要特別使用 -l 來指定 landscape 排版，亦即 dvipdfmx -l yzu_coverbridge.dvi。由於中文字直排的字型資料較缺乏製作資訊，建議只使用有 CJK 套件原裝資料的 bkai (楷體) 或 bsmi (明體)。


** 修改格式配合其他學校規定

yzu_thesis.lyx 裏面可能要改的是頁面四邊的留白: tmargin, bmargin, lmargin, rmargin; 行距，段落之間的間隔，全篇預設的中文字體，完全關掉浮水印，完全關掉中文數字的章別。

yzu_frontpages.tex 關於封面、書名頁、中文摘要、英文摘要、誌謝、目錄、表目錄、圖目錄、符號說明
等頁之格式。

yzu_backpages.lyx 關於參考文獻所使用的格式 (預設是 ieeetr.bst)，以及附錄、自傳頁面的格式。

yzu_watermark.tex 浮水印圖檔呈現的大小、位置如有不同，要修改此檔。如果只有少數幾頁需要浮水印，則把此檔內特定幾行關閉即可，位於 
%% >>> 全篇浮水印
與
%% <<< 全篇浮水印
之間。請看檔內註解說明。

yzu_definitions.tex 如果對於 LaTeX 使用的特定名詞 (Figure, Table, Chapter, References) 的中文對應詞 (圖，表，第 x 章) 有所不同，則修改此檔內的設定。

yzu_chnum.tex 中文數字的章別，如何呈現在目錄裏，可能有不同的作法。可以參考檔內的註解加以修改。




** Version History:

* v2.0 (4/5/2009)
 - 利用 LaTeX-CJK 套件 4.7 版的新功能，CJK 套件載入的是 CJKutf8。這可以讓 pdflatex 工作流程也可以產生可搜尋、拷貝的中文字串的 PDF 檔。為了解決在第二輪編譯時，toc 部份會出問題，在最後 \end{CJK}之前，加入 \clearpage。這是參考了 LaTeX-CJK 套件裏的說明文件 CJK.txt。修改了 yzu_thesis.tex。
 - 章名裏的章別，可以用中文數字，例如「第一章」。元智大學論文規範，從以前就是這樣規定。但是過去幾版的 yzu_thesis template, 並沒有找到方法做如此的排版。現在剛好有成大的詹魁元教授詢問，就一勞永逸，把它做出來了。修改了 yzu_report.cls, yzu_thesis.tex。目錄裏的呈現，可以是底下的各種組合
	1  簡介 ............................ 1
	一、簡介 ............................ 1
	第一章　簡介 ......................... 1
	第一章、簡介 ......................... 1
使用上很有彈性。相關設定在 yzu_chnum.tex 裏。
 - 把原本在 yzu_thesis.tex 裏關於各個排版相關的內定字詞 (Figure, Table, Chapter) 等的中文對應，移至 yzu_definitions.tex 裏。
 - 加入 hyperref 套件，可以產生具有超連結 (由目錄跳至特定章節) 之 pdf 檔。TeX 系統版本要求至少是 TeXLive2008。更改了 yzu_thesis.tex, yzu_frontpages.tex, yzu_backpages.tex, my_appendix.tex。
 - yzu_coverbridge.tex 畢業級別的兩位數，中線對得較準了。更改了 yzu_coverbridge.tex。
 - 同步釋出 LyX 可以用的格式檔。LyX 版本要求至少是 v1.6.2。 

陳念波
npchen at saturn.yzu.edu.tw
Apr 5, 2009