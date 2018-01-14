# 課題8レポート

「ぱくたそ」から持ってきた画像を原画像とする．この画像は縦1066画素，横1600画素によるディジタルカラー画像である．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai8/Cat3.jpg)  
図1 原画像

ORG = imread('Cat.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示   

によって，原画像を読み込み，グレースケールで表示した結果を図2に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai8/kadai8_1.jpg)  
図2 原画像(グレースケール)

図2を閾値128で2値化したものを図3に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai8/kadai8_2.jpg)  
図3 2値化画像

次に，図2をラベリングしたものを図4に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai8/kadai8_3.jpg)  
図4 ラベリング画像

ラベリングとは，同じ連結成分に属する画素に同一番号を，異なる連結成分に異なる番号を与える処理の事である．
図4より，図3の2値化画像がラベリングされ，領域ごとに分けられ，それらの特徴や数などを調べることができる．
