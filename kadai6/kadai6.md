

# 課題6レポート

「ぱくたそ」から持ってきた画像を原画像とする．この画像は縦1066画素，横1600画素によるディジタルカラー画像である．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai6/Cat.jpg)  
図1 原画像

ORG=imread('Cat.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって，原画像を読み込み，グレースケールで表示した結果を図2に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai6/kadai6_1.jpg)  
図2 原画像(グレースケール)

閾値128を用いて2値化した画像を図3に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai6/kadai6_2.jpg)  
図3 2値化画像

ディザ法を用いて2値化した画像を図4に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai6/kadai6_3.jpg)  
図4 2値化画像(ディザ法)



