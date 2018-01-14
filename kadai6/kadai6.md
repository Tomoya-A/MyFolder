

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

ディザ法とは，原画像の各画素の濃度値をあらかじめ画素位置により定められた閾値(ディザマトリクス)と比較し，その大小関係で出力画素の濃度値を決定する方法である．また，matlabのdither関数では，フロイド-スタインバーグ・ディザリングというアルゴリズムが用いられている．
こういったアルゴリズムを用いることで，少階調しか表示できない装置で，多階調を表現することができる．図3と図4を比べると一目瞭然で，どちらも2値の濃度値しか使っていないが，明らかにディザ法を用いた画像の方が原画像の濃淡に忠実であることがわかる．
