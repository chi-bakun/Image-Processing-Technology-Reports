# 課題1レポート
標準画を「chi_bakun.png」とする。
この画像は縦275画素、横183画素によるディジタルカラー画像である。

ORG = imread('chi_bakun.png'); %原画像の入力
imageesc(ORG); axis image; %画像表示

によって、原画像を読み込み、表示した結果を図1に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai1/kadai1_1.png)

図1


原画像を1/2サンプリングするためには、画像を1/2倍に縮小した後に2倍すればよい。拡大する際には、単純補間するために「box」オプションを設定する。

IMG = imresize(ORG,0.5); % 画像の縮小

IMG2 = imresize(IMG,2,'box'); % 画像の拡大

結果を図2に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai1/kadai1_2.png)

図2


1/2サンプリング同様に原画像を1/4サンプリングするには、
画像を1/2倍に縮小した後、2倍に拡大すればよい。すなわち、

IMG = imresize(ORG,0.5); % 画像の縮小 

IMG2 = imresize(IMG,2,'box'); % 画像の拡大

とする．1/4サンプリングの結果を図3に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai1/kadai1_3.png)

図3


1/4サンプリング、1/8から1/32サンプリングは、

IMG = imresize(ORG,0.5); % 画像の縮小 

IMG2 = imresize(IMG,2,'box'); % 画像の拡大

を繰り返す．サンプリングの結果を図４～６に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai1/kadai1_4.png)

図4

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai1/kadai1_5.png)

図5

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai1/kadai1_6.png)

図6
