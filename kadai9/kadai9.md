# 課題9レポート

「ぱくたそ」から持ってきた画像を原画像とする．この画像は縦1066画素，横1600画素によるディジタルカラー画像である．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai9/Cat.jpg)  
図1 原画像

ORG = imread('Cat.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示   

によって，原画像を読み込み，グレースケールで表示した結果を図2に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai9/kadai9_1.jpg)  
図2 原画像(グレースケール)

を図3に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai9/kadai9_2.jpg)  
図3 

を図4に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai9/kadai9_3.jpg)  
図4 

を図5に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai9/kadai9_4.jpg)  
図5 

を図6に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai9/kadai9_5.jpg)  
図6 





