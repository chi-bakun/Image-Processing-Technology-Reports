# 課題7レポート

課題7　ダイナミックレンジの拡大
画素のダイナミックレンジを０から２５５にせよ。
下記はサンプルプログラムである。
課題作成にあたっては「Lenna」以外の画像を用いよ。

ORG = imread('chi_bakun.png'); % 画像の読み込み

ORG = rgb2gray(ORG); % 白黒濃淡画像に変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

pause;

原画像を白黒濃淡画像に変換した結果を図1に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai7/kadai7_1.png)

図1

imhist(ORG); % 濃度ヒストグラムを生成、表示

pause;

ヒストグラムは図2に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai7/kadai7_2.png)

図2


ダイナミックレンジを設定する。

ORG = double(ORG);

mn = min(ORG(:)); % 濃度値の最小値を算出

mx = max(ORG(:)); % 濃度値の最大値を算出

ORG = (ORG-mn)/(mx-mn)*255;

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

pause;

結果を図3に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai7/kadai7_3.png)

図3


ORG = uint8(ORG); % この行について考察せよ

imhist(ORG); % 濃度ヒストグラムを生成、表示

ヒストグラムは図4に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai7/kadai7_4.png)

図4

ORG = uint8(ORG);
は、
ORG = (ORG-mn)/(mx-mn)*255
によって小数が表れるので、それを整数へ変換している。


また、ダイナミックレンジを125にした原画像を図5、ヒストグラムを図6に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai7/kadai7_5.png)

図5

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai7/kadai7_5.png)

図6