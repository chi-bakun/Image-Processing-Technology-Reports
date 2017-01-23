# 課題8レポート

課題８ ラベリング 
二値化された画像の連結成分にラベルをつけよ。 
下記はサンプルプログラムである。
課題作成にあたっては「Lenna」以外の画像を用いよ。

ORG = imread('chi_bakun.png'); % 画像の読み込み 

ORG = rgb2gray(ORG); % 白黒濃淡画像に変換 

imagesc(ORG); colormap(gray); colorbar; % 画像の表示 

pause; 

原画像を白黒濃淡画像に変換した結果を図1に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai8/kadai8-1.png)

図1

閾値を128に設定し、2値化する。

IMG = ORG > 128; % 閾値128で二値化 

imagesc(IMG); colormap(gray); colorbar; % 画像の表示 

pause; 

結果を図2に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai8/kadai8-2.png)

図2


画像にラベルをつける。

IMG = bwlabeln(IMG); 

imagesc(IMG); colormap(jet); colorbar; % 画像の表示 

pause;

結果を図3に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai8/kadai8-3.png)

図3