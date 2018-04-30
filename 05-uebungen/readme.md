# Matlab Übungen 01 

## Code Matlab 

> a) Schreiben Sie Funktionen zur Berechnung folgender Bildstatistiken:
> b) -Mittlerer Grauwert


``` Matlab
function out = medianGray(in)
    [x,y] = size(in);
    out = sum(sum(in))/x/y;
end
``` 

> c) -Mittlere quadratische Abweichung

``` Matlab
function out = medianQuadDifference(in)
    out = std2(in)^2/0.25*100;
end
``` 