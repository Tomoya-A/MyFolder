
# 課題4レポート

「ぱくたそ」から持ってきた画像を原画像とする．この画像は縦1066画素，横1600画素によるディジタルカラー画像である．

ORG=imread('Cat.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって，原画像を読み込み，グレースケールで表示した結果を図１に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai4/kadai4_1.jpg)  
図1 原画像(グレースケール)

図1のヒストグラムを図2に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai4/kadai4_2.jpg)  
図2 ヒストグラム

図2を見ると，0～50の範囲に1つ山があり，そこより後ろの範囲にもう1つ山があることがわかる．おそらく0～50の範囲の山は図1の右側にある黒い部分であり，もう1つの山は猫の顔や体の白い部分であると考えられる．
