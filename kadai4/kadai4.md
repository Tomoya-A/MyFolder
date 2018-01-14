
# 課題3レポート

「ぱくたそ」から持ってきた画像を原画像とする．この画像は縦1066画素，横1600画素によるディジタルカラー画像である．

ORG=imread('Cat.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって，原画像を読み込み，グレースケールで表示した結果を図１に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai4/kadai4_1.jpg)  
図1 原画像(グレースケール)

まず，閾値に輝度値64を設定するために，IMG = ORG > 64;とする．これにより，IMGにはORGの輝度値64以上の画素を白(1)，64未満の画素を黒(0)に変換した画像が格納されている．

輝度値を64とした結果を図2に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai3/kadai3_2.jpg)  
図2 輝度値64

