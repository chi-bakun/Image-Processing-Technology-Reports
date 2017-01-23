# 課題3レポート

閾値を4パターン設定し、閾値処理した画像を示せ。
課題作成にあたっては「Lenna」以外の画像を用いよ

clear; % 変数のオールクリア

ORG=imread('chi_bakun.png'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

pause;

原画像を白黒濃淡画像に変換した結果を図1に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai3/kadai3_1.png)

図1

閾値を64に設定する。

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

pause;

結果を図2に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai3/kadai3_2.png)

図2


同様にし、閾値を96に設定する。

IMG = ORG > 96; % 輝度値が96以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

pause;

結果を図3に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai3/kadai3_3.png)

図3


同様にし、閾値を128に設定する。

IMG = ORG > 128; % 輝度値が128以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

pause;

結果を図4に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai3/kadai3_4.png)

図4

同様にし、閾値を196に設定する。

IMG = ORG > 192; % 輝度値が192以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

結果を図5に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai3/kadai3_5.png)

図5