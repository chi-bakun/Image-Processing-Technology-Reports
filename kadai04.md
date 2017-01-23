# 課題4レポート

画素の濃度ヒストグラムを生成せよ。
課題作成にあたっては「Lenna」以外の画像を用いよ

濃度のヒストグラムは、まず原画像を白黒濃淡画像に変換する。
その後、MATLABのimhist()関数を用いて表示をする。


clear; % 変数のオールクリア

ORG=imread('chi_bakun.png'); % 原画像の入力

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

pause;

imhist(ORG); % ヒストグラムの表示

原画像を白黒濃淡画像に変換した結果を図1に示す。


![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai4/kadai4_1.png)

図1

この画像のヒストグラムは図2に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai4/kadai4_2.png)

図2
