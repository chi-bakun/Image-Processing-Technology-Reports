# 課題1レポート
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
