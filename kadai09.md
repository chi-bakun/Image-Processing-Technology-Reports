# 課題9レポート

課題９ メディアンフィルタと先鋭化 
メディアンフィルターを適用し、ノイズ除去を体験せよ。 
各自，Lenna以外の画像を用いよ。

ORG = imread('chi_bakun.png'); % 画像の読み込み 

ORG = rgb2gray(ORG); % 白黒濃淡画像に変換 

imagesc(ORG); colormap(gray); colorbar; % 画像の表示 

pause;

原画像を白黒濃淡画像に変換した結果を図1に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai9/kadai9_1.png)

図1

画像にノイズを付与する。

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付 

imagesc(ORG); colormap(gray); colorbar; % 画像の表示 

pause; 

結果を図2に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai9/kadai9_2.png)

図2


「平滑化フィルタ」によってノイズを除去する。

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去 

imagesc(IMG); colormap(gray); colorbar; % 画像の表示 

pause; 

結果を図3に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai9/kadai9_3.png)

図3


「メディアンフィルタ」によってノイズを除去する。

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去 

imagesc(IMG); colormap(gray); colorbar; % 画像の表示 

pause; 

結果を図4に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai9/kadai9_4.png)

図4

「ディジタルフィルタ」の値を設定し、フィルタを適用する。

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計 

IMG = filter2(f,IMG,'same'); % フィルタの適用
 
imagesc(IMG); colormap(gray); colorbar; % 画像の表示 

pause; 

結果を図5に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai9/kadai9_5.png)

図5