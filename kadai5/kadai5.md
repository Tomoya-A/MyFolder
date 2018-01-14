
# 課題5レポート

「ぱくたそ」から持ってきた画像を原画像とする．この画像は縦1066画素，横1600画素によるディジタルカラー画像である．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai5/Cat.jpg)  
図1 原画像

ORG=imread('Cat.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって，原画像を読み込み，グレースケールで表示した結果を図2に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai5/kadai5_1.jpg)  
図2 原画像(グレースケール)

判別分析法を用いて2値化した画像を図3に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai5/kadai5_2.jpg)  
図3 2値化画像

判別分析法とは，対象物の濃度と，背景の濃度とがそれぞれ最も良くまとまり，かつ対象物と背景との違いが際立つように閾値を定める方法である．図3だけだとわかりづらいので，他に2種類画像を用意し，同様に判別分析法を用いて2値化してみた．

以下に示す2種類ともに「ぱくたそ」から持ってきた画像であり，どちらも縦900画素，横1600画素によるディジタルカラー画像である．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai5/Cat2.jpg)  
図4 原画像2

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai5/Cat3.jpg)  
図5 原画像3

また，それぞれのグレースケール画像と2値化した画像を図6～図9に示す．

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai5/kadai5_3.jpg)  
図6 原画像2(グレースケール)

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai5/kadai5_4.jpg)  
図7 原画像2の2値化画像

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai5/kadai5_5.jpg)  
図8 原画像3(グレースケール)

![原画像](https://github.com/Tomoya-A/MyFolder/blob/master/kadai5/kadai5_6.jpg)  
図9 原画像3の2値化画像

ここで，これらの結果を比べてみると，図6は背景と対象物の違いが見てとれるが，図9は全く違いがわからなくなってしまっている．理由としては，背景と対象物の色が近いためであると考えられる．したがって，判別分析法を用いる場合には，背景と対象物の色の違いがはっきりしている画像を選ぶことが大切である．
