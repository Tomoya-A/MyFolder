# 課題7レポート

「ぱくたそ」から持ってきた画像を原画像とする．この画像は縦1066画素，横1600画素によるディジタルカラー画像である．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai7/Cat.jpg)  
図1 原画像

ORG = imread('Cat.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示   

によって，原画像を読み込み，グレースケールで表示した結果を図2に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai7/kadai7_1.jpg)  
図2 原画像(グレースケール)

図2のヒストグラムを図3に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai7/kadai7_2.jpg)  
図3 図2のヒストグラム

次に，図2のダイナミックレンジを拡大したものを図4に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai7/kadai7_3.jpg)  
図4 ダイナミックレンジ拡大

図4のヒストグラムを図5に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai7/kadai7_4.jpg)  
図5 図4のヒストグラム

図3と図5を比較すると，ダイナミックレンジを拡大することで濃度値の範囲が最小最大方向に広がっていることがわかる．
また，ORG = uint8(ORG);により，倍精度のdouble型から符号なし整数のint型に変換されている．これにより，精度が高い型から低い型に変換することで丸められるため，図5のヒストグラムでは，等間隔ごとに濃度値がないところが出来ている．
