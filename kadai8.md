# 課題５レポート

標準画像は課題2に使用した「GirDog」を原画像とする．この画像は縦611画像，横450画素による正方形のディジタルカラー画像である．

ORG = imread('GirDog.png'); % 画像の読み込み 
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示 
pause;  

によって，原画像を読み込み，白黒濃淡画像へ変換し，表示した結果を図１に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kekka8-1.png)  

図1 白黒濃淡画像

しきい値128で二値化をするにはい以下のコマンドを実行する．

IMG = ORG > 128; % 閾値128で二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示 
pause;  

実行結果は図2に示す。

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kekka8-2.png)  

