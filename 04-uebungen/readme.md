# Matlab Übungen 03

``` Matlab

rgb2 = zeros(512,512, 3)
rechts = im2double(rechts512);
links  = im2double(links512);
rgb2(:,:,1)= links;
rgb2(:,:,2)= rechts;
imshow(rgb2);

``` 