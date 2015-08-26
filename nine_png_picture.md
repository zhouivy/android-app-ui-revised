## **.9.png自适应调节大小圖片詳解** ##

**.9.png圖片介紹**

.9.PNG是安卓开发里面的一种特殊的图片
这种格式的图片在android 环境下具有自适应调节大小的能力。
（1）允许开发人员定义可扩展区域，当需要延伸图片以填充比图片本身更大区域时，可扩展区的内容被延展。
（2）允许开发人员定义内容显示区，用于显示文字或其他内容。

**.9.png圖片製作**

製作該類圖片需要使用到java的jdk、android的sdk中tools目录下的draw9patch.bat工具。
打開該工具後會看到如圖所示。
工具節目左側為圖片編輯區域，右側為編輯後效果顯示區域。
下方的“Zoom”和“Patch scale”分別調節左側編輯區域大小和右側拉伸拉伸大小。

編輯區域圖片的左侧和上方的黑线交叉的部分即為自定義的可扩展区域，上端的黑色横条表示图片在水平方向上可以拉伸的区域（即黑色橫條部分以下），左边的黑色横条表示图片可以在竖直方向上被拉伸的区域（黑色豎條以右）；右侧和下方的黑线交叉的部分即内容显示区域(如做button背景图时，button上文字的显示区域)；紅灰色斜線區域為不能編輯部分，編輯時只需鼠標左右鍵點擊邊框部分即可。
<img src='https://lh4.googleusercontent.com/-G_a70DjYJtE/Uh1f4KTpNcI/AAAAAAAAWzQ/IAZaPHUa4sY/w1003-h587-no/%25E6%258D%2595%25E8%258E%25B7.PNG' width='100%'>

製作完成後保存圖片，工具將會以.9.png後綴名保存。此時的圖片是帶有黑線的，但是已經可以使用，對於開發者來說可以直接放到素材裡，經過開發工具編譯成apk之後會自動消除黑線保留黑線的信息，也可以使用apktool等反編譯工具，進行回編譯時，也會去除黑線。<br>
<br>
<b>使用xUltimate-d9pc-x86工具去除黑線</b>

<a href='https://code.google.com/p/android-app-ui-revised/issues/detail?id=1#c5'>點擊下載xUltimate-d9pc-x86工具</a>

把要去除黑线的图片放到example1\res\drawable-hdpi目录下，然后点击xUltimate-d9pc.exe，运行，等一两秒，滴答一声就完成了去除黑线。处理好的.9图片在done\example1\res\drawable-hdpi 目录下，把图片复制出来就可以用了。<br>
適用於直接把apk解壓出來的修改者。