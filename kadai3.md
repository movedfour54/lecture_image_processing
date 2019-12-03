# 課題３レポート

標準画像「zim」を原画像とする．この画像は縦1473画像，横600画素による正方形のディジタルカラー画像である．

ORG=imread('zim.png'); % 原画像の入力  

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/zim.png?raw=true)  

図1 原画像

原画像を白黒に更新するには以下のコマンドを実行する．

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換                     
imagesc(ORG); colormap(gray); colorbar; % 画像の表示                   


その結果を図２に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kadai%203-1.png?raw=true)  
図2 白黒の画像

しきい値を64に設定をするには以下のコマンドを実行する．

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換          
imagesc(IMG); colormap(gray); colorbar;　　　　　　　　　　　　　　　

その結果を図３に示す．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kadai%203-2.png?raw=true)  
図3 しきい値が64の結果

同様に、他のしきい値を設定した結果は以下のようになった．

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kadai%203-3.png?raw=true)  
図4 しきい値が96の結果

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kadai%203-4.png?raw=true)  
図5 しきい値が128の結果

![原画像](https://github.com/movedfour54/lecture_image_processing/blob/master/image/kadai%203-5.png?raw=true)  
図6 しきい値が192の結果



このように階調された画像を示すことができる．
