# 課題10レポート

課題10 画像のエッジ抽出  
次のプログラムを参考にして、エッジ抽出を体験せよ。
各自、Lenna以外の画像を用いよ。

ORG = imread('chi_bakun.png'); % 原画像の入力 

ORG = rgb2gray(ORG); %カラーからグレイへの変換 

imagesc(ORG); colormap('gray'); colorbar;% 画像表示 

pause; % 一時停止

原画像を白黒濃淡画像に変換した結果を図1に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai10/kadai10_1.png)

図1

「プレウィット法」によってエッジを抽出する。

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）
 
imagesc(IMG); colormap('gray'); colorbar;% 画像表示 

pause; % 一時停止 

結果を図2に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai10/kadai10_2.png)

図2


「ソベル法」によってエッジを抽出する。

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）
 
imagesc(IMG); colormap('gray'); colorbar;% 画像表示 

pause; % 一時停止

結果を図3に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai10/kadai10_3.png)

図3


「キャニー法」によってエッジを抽出する。

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）
 
imagesc(IMG); colormap('gray'); colorbar;% 画像表示 

pause; % 一時停止 

結果を図4に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai10/kadai10_4.png)

図4