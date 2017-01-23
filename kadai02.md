# 課題2レポート

2階調、4階調、8階調の画像を生成せよ。
課題作成にあたっては「Lenna」以外の画像を用いよ

clear; % 変数のオールクリア

ORG=imread('chi_bakun.png'); % 原画像の入力

ORG = rgb2gray(ORG); colormap(gray); colorbar;

imagesc(ORG); axis image; % 画像の表示

pause; % 一時停止

原画像をグレーに変換した結果を図1に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai2/kadai2_1.png)

図1

この画像を2階調で表すためには、閾値を 256 / 2 = 128 に設定する。

% ２階調画像の生成

IMG = ORG>128;

imagesc(IMG); colormap(gray); colorbar;  axis image;

pause;

結果を図2に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai2/kadai2_2.png)

図2


同様にし、4階調で表すには閾値を 256 / 4 = 64 すなわち、64、128、192に設定する。

% ４階調画像の生成

IMG0 = ORG>64;

IMG1 = ORG>128;

IMG2 = ORG>192;

IMG = IMG0 + IMG1 + IMG2;

imagesc(IMG); colormap(gray); colorbar;  axis image;

結果を図3に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai2/kadai2_3.png)

図3


同様にし、8階調は閾値を 256 / 8 = 32 すなわち、32、64、96、128、160、192、224に設定する。

% ８階調画像の生成

IMG0 = ORG>32;

IMG1 = ORG>64;

IMG2 = ORG>96;

IMG3 = ORG>128;

IMG4 = ORG>160;

IMG5 = ORG>192;

IMG6 = ORG>224;

IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;

imagesc(IMG); colormap(gray); colorbar;  axis image;

結果を図4に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai1/kadai2_4.png)

図4