# Matlab Übungen 03

> a) Laden Sie das Stereobildpaar 'links.mat' und 'rechts.mat' mit der Funktion 'load'
> b) Erzeugen Sie ein RGB-Bild
> c) Kopieren Sie die Bildmatrix 'links512' in den Rot-Kanal
> d) Kopieren Sie die Bildmatrix 'rechts512' in den Grün- und BlauKanal
> e) Geben Sie RGB-Bild auf den Bildschirm aus und betrachten Sie es mit einer Rot-Cyan-Brille

## Lösung

``` Matlab

rgb2 = zeros(512,512, 3)
rechts = im2double(rechts512);
links  = im2double(links512);
rgb2(:,:,1)= links;
rgb2(:,:,2)= rechts;
imshow(rgb2);

``` 