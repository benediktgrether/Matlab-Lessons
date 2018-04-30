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

> d) -Histogramm

```Matlab
function out = histogramNew(in)    
    [x,y] = size(in);    
    li = uint8(in*(x/2));
    li = li(:);
    histo= zeros(x/2,1);
    for k = 1:(x*y)
        histo(li(k)+1) = histo(li(k)+1)+1;
    end
       %out = histo;
       %bar(histo);
       bar(histo/x/y);
end
``` 
