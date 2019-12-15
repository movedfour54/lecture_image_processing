# 課題４レポート

標準画像「Gir」を原画像とする．この画像は縦960画像，横511画素による正方形のディジタルカラー画像である．

ORG=imread('Gir.jpg'); % 原画像の入力  

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/org_img.png)  
図1 原画像

原画像を白黒濃淡画像へ変換するには以下の駒dのを実行する．

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

白黒濃淡画像の結果を図２に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kadai%206.png)  
図2 白黒濃淡画像

以上でカラー画像を白黒濃淡画像へ変換方法であった．
