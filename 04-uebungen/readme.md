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

> g) Nehmen Sie ein Stereobildpaar mit der Web-Cam auf (siehe Übungsblatt 3), und achten Sie auf folgende Dinge:
> h) -Es sollten näherungsweise nur horizontale Verschiebungen auftreten
>i) -Die Verschiebungen dürfen nur gering sein
>j) -Es dürfen keine bewegten Objekte vorhanden sein, wenn Sie ein Bildpaar nacheinander mit einer Kamera aufnehmen (warum?)
> k) Duplizieren Sie das Bildpaar im Workspace und wandeln Sie es in in ein Grauwert-Bildpaar vom Typ double um
> l) Achten Sie auf den Wertebereich!
> m)Stellen Sie dieses Bildpaar ebenso dar wie das Bildpaar 'links512' und 'rechts512'
> n) Vergleichen Sie die Ergebnisse


``` Matlab
rgb3=zeros(720,1080,3);
benelinks = im2double(bene_1);
benerechts = im2double(bene_2);
beneLinks = rgb2gray(benelinks);
beneRechts = rgb2gray(benerechts);

rgb3(:,:,1)= beneLinks;
rgb3(:,:,2)= beneRechts;
imshow(rbg3);

```