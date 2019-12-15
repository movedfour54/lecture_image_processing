# 課題６レポート

標準画像は図3に使用した「zim」を原画像とする．この画像は縦1473画像，横600画素による正方形のディジタルカラー画像である．

ORG=imread('zim.png'); % 原画像の入力 
ORG = rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示 
pause; % 一時停止 

によって，原画像を読み込み，白黒濃淡画像へ変換し，表示した結果を図１に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kekka6-1.png?raw=true)  

図1 白黒濃淡画像

輝度値が128によって二値化にするには以下のコマンドを実行する．

IMG = ORG>128; % 128による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示 
pause;  

実行結果は図２に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kekka6-2.png?raw=true)  

図2 二値化された画像

ディザ法による二値化をするには以下のコマンドを実行する．

IMG = dither(ORG); % ディザ法による二値化 
imagesc(IMG); colormap(gray); colorbar; % 画像の表示 

実行結果は図3に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kekka6-3.png?raw=true)  

図3 ディザ法による二値化された画像
