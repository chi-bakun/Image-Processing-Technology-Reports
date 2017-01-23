# 課題5レポート

判別分析法を用いて画像二値化せよ。
課題作成にあたっては「Lenna」以外の画像を用いよ

判別分析法とは、画素を2つのクラスに分けて
クラス内分散が最小かつクラス間分散が最大になるように閾値を決める方法である。

ORG=imread('chi_bakun.png'); % 原画像の入力

ORG = rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

pause;

まずは、原画像を入力し白黒濃淡画像に変換する。

H = imhist(ORG); %ヒストグラムのデータを列ベクトルEに格納
myu_T = mean(H);

max_val = 0;

max_thres = 1;

for i=1:255

C1 = H(1:i); %ヒストグラムを2つのクラスに分ける

C2 = H(i+1:256);

n1 = sum(C1); %画素数の算出

n2 = sum(C2);

myu1 = mean(C1); %平均値の算出

myu2 = mean(C2);

sigma1 = var(C1); %分散の算出

sigma2 = var(C2);

sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出

sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出

if max_val<sigma_B/sigma_w

max_val = sigma_B/sigma_w;

max_thres =i;

end;

end;

その後濃度ヒストグラムのデータ列をベクトルに格納し、平均をとる。
クラスを2つに分けて、クラスごとの画素数を算出し、平均値を計算する。
さらに、クラス内分散とクラス間分散を算出し、(クラス間分散) / (クラス内分散) > 0　を満たすiを
求め、それを閾値をしている。

元の白黒濃淡画像を図1に
判定分析法によって求めた閾値によって2値化した画像は図2に示す。

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai5/kadai5_1.png)

図1

![原画像](https://github.com/chi-bakun/Image-Processing-Technology-Reports/blob/master/image/kadai5/kadai5_2.png)

図2

相性が悪かったのか、むしろ悪化してしまった。