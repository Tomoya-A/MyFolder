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

図2にごま塩ノイズを加えたものを図3に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai9/kadai9_2.jpg)  
図3 ごま塩ノイズ

図3に平均化フィルタをかけたものを図4に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai9/kadai9_3.jpg)  
図4 平均化フィルタ

図3にメディアンフィルタをかけたものを図5に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai9/kadai9_4.jpg)  
図5 メディアンフィルタ

また，設計したフィルタをかけたものを図6に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai9/kadai9_5.jpg)  
図6 設計フィルタ

ごま塩フィルタは，ORG = imnoise(ORG,'salt & pepper',0.02);で行われている．これは，0と255の画素を散りばめるノイズである．また，0.02というのは2%の添付率を表している．
平均化フィルタとは，着目画素とその八近傍の平均値から算出するフィルタであり，図4を見てわかる通り少しぼやけてしまう．これにより，ノイズが多少は軽減されたが，それでもまだ見てわかるくらいには残っている．
メディアンフィルタとは，変換後の濃度値を着目画素の近傍画素の濃度値の中央値とする方法である．これにより，ぼやけずにノイズを完全に除去できていることがわかる．
設計フィルタは，f=[0,-1,0;-1,5,-1;0,-1,0];というフィルタを設計し，これを適用しているものである．このフィルタは，鮮鋭化フィルタと呼ばれ，画像の濃度値の変化を強調して表現するものである．これを適用するとなぜ灰色になるかはよくわからなかった．

