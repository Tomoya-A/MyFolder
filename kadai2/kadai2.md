# 課題2レポート

「ぱくたそ」から持ってきた画像を原画像とする．この画像は縦1066画素，横1600画素によるディジタルカラー画像である．

ORG=imread('Cat.jpg'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，グレースケールで表示した結果を図１に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai2/kadai2_1.jpg)  
図1 原画像(グレースケール)

図1を2階調画像にするには，まず黒(0)と白(1)を区別する閾値が必要となる．閾値は256/階調数で求めることができるので，2階調であれば256/2=128となる．したがって，IMG = ORG>128;において128より大きいものは白(1)，128未満のものは黒(0)となり，2階調画像が実現できる．

図1を2階調画像とした結果を図2に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai2/kadai2_2.jpg)  
図2 2階調画像

同様に，4階調画像も考える．まず256を等間隔にするために閾値が3つ必要となるので，256/4=64と，その2倍3倍した128，192を閾値とする．
IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
上記のプログラムのIMG0，IMG1，IMG2には各閾値での2階調画像が格納されており，それらの和で4階調画像が実現される．

図1を4階調画像とした結果を図3に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai2/kadai2_3.jpg)  
図3 4階調画像

同様にして8階調画像とした結果を図4に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai2/kadai2_4.jpg)  
図4 8階調画像

このようにサンプリング幅が大きくなると，モザイク状のサンプリング歪みが発生する．
