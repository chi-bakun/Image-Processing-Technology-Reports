# 課題6レポート

課題６　画像の二値化 
下記のプログラムを参考にして画像を二値化せよ。 
下記はサンプルプログラムである。
課題作成にあたっては「Lenna」以外の画像を用いよ。

clear; % 変数のオールクリア

ORG=imread('chi_bakun.png'); % 原画像の入力

ORG = rgb2gray(ORG);

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

pause; % 一時停止

原画像を白黒濃淡画像に変換した結果を図1に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai6/kadai6_1.png)

図1

閾値を1238設定し、2値化する。

IMG = ORG>128; % 128による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

pause;

結果を図2に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai6/kadai6_2.png)

図2


次はディザ法によって2値化する。

IMG = dither(ORG); % ディザ法による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

結果を図3に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai6/kadai6_3.png)

図3