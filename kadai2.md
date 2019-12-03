# 課題２レポート

標準画像「GirDog」を原画像とする．この画像は縦611画像，横450画素による正方形のディジタルカラー画像である．

ORG=imread('GirDog.png'); % 原画像の入力  

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/GirDog.png?raw=true)  

図1 原画像

原画像を白黒に更新するには以下のコマンドを実行する．

ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示

その結果を図２に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kadai%202-2.png?raw=true)  
図2 白黒の画像

画像を2階調にするには以下のコマンドを実行する．

IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;

その結果を図３に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kadai%202-3.png?raw=true)  
図3 2階調の画像

画像を4階調にするには以下のコマンドを実行する．

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
imagesc(IMG); colormap(gray); colorbar;  axis image;

その結果を図4に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kadai%202-4.png?raw=true)  
図4 4階調の画像

画像を8階調にするには以下のコマンドを実行する．

IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>96;
IMG3 = ORG>128;
IMG4 = ORG>160;
IMG5 = ORG>192;
IMG6 = ORG>224;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 +IMG6;
imagesc(IMG); colormap(gray); colorbar;  axis image;

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kadai%202-5.png?raw=true)  
図5 8階調の画像

このように階調された画像を示すことができる．
