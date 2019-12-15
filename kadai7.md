#課題７レポート

標準画像は課題1及び課題4に使用した「Gir」を原画像とする．この画像は縦960画像，横511画素による正方形のディジタルカラー画像である．  

ORG = imread('Gir.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示 
pause;  

によって，原画像を読み込み，白黒濃淡画像へ変換し，表示した結果を図１に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kekka7-1.png)  

図1 白黒濃淡画像

濃度ヒストグラムを作成するには以下のコマンドを実行する．

imhist(ORG); % 濃度ヒストグラムを生成、表示 
pause;  

実行結果は図2に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kekka7-2.png)  

図2　濃度ヒストグラム

その後、以下のコマンドを実行した．

ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255; 
imagesc(ORG); colormap(gray); colorbar; % 画像の表示 
pause;  

実行結果は図3に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kekka7-3.png)  

図3　実行結果の画像

図3に示させた画像の濃度ヒストグラムは以下のコマンドの実行で示す．

ORG = uint8(ORG); % この行について考察せよ
imhist(ORG); % 濃度ヒストグラムを生成、表示

実行結果は図4に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kekka7-4.png)
