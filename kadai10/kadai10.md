
# 課題10レポート

「ぱくたそ」から持ってきた画像を原画像とする．この画像は縦1066画素，横1600画素によるディジタルカラー画像である．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai10/Cat.jpg)  
図1 原画像

ORG = imread('Cat.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); %カラーからグレイへの変換  
imagesc(ORG); colormap('gray'); colorbar;% 画像表示    

によって，原画像を読み込み，グレースケールで表示した結果を図2に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai10/kadai10_1.jpg)  
図2 原画像(グレースケール)

図2をプレウィット法を用いてエッジ抽出したものを図3に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai10/kadai10_2.jpg)  
図3 プレウィット法

図2をソベル法を用いてエッジ抽出したものを図4に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai10/kadai10_3.jpg)  
図4 ソベル法

図2をキャニー法を用いてエッジ抽出したものを図5に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai10/kadai10_4.jpg)  
図5 キャニー法

プレウィット法とは，3画素ずつを対にして濃度の変化点を抽出する処理であり，ソベル法は，中心画素の影響を強調した処理である．図3と図4を比較すると，どちらも同じように見え大した変化は見当たらない．
キャニー法は，上記2つより強力なエッジ検出法である．したがって，上記2つの結果と比べてみても違いが一目瞭然である．キャニー法を用いた方がプレウィット法，ソベル法では見られなかった部分のエッジも抽出し，より明瞭になっていることがわかる．
