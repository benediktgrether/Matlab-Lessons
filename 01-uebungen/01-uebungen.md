# Matlab Übungen 01 

> **c.) Erzeugen Sie ein kleines Bild (z.B. 16x16) mit einem Bayer-Pattern**
>

## Code Matlab 
``` Matlab

    b = zeros(16, 16, 3);
    
    % Farbe Rot
    b(1:2:end, 2:2:end, 1) = 1;

    % 1:2:end | 1 = erste Zeile , 2 = 2 Wert bis zum Ende.
    % 2:2:end | 2 = jede zweite Zeile , jeder 2 Wert bis zum Ende.
    % 1 | 1 Bekommt die Farbe Rot. 

    b(2:2:end, 1:2:end, 3) = 1;
    
    % 2:2:end | 2 = zweite Zeile, 2 = zweiter Wert bis zum Ende
    % 1:2:end | 1 = jede erste Zeile, 2 = jeder zweiter Wert bis zum Ende. 
    3 | 3 Bekommt die Farbe Blau.

    b(1:2:end, 1:2:end, 2) = 1;
    
    % 1:2:end | 1 = erste Zeile , 2 = 2 Wert bis zum Ende.
    % 1:2:end | 1 = jede erste Zeile , 2 = jeder zweite Wert bis zum Ende.
    2 | 2 Bekommt die Farbe Grün

    b(2:2:end, 2:2:end, 2) = 1;
    % 2:2:end | 2 = zweite Zeile, 2 = zweiter Wert bis zum Ende
    % 2:2:end | 2 = jede zweite Zeile , jeder 2 Wert bis zum Ende.
    2 | 2 Bekommt die Farbe Grün
    
    imtool(b)

```

> **d.) Wandeln Sie ein RGB-Farbbild in ein Bayer-Pattern-Bild um**
>
> Ist noch nicht fertig. 

## Code Matlab 
``` 
    b=zeros(512,512,3);
    b(2:2:end,2:2:end,3)=lena_std(2:2:end,2:2:end,3);
    imshow(b)


```


## Code Matlab 
``` 
    bb=b(:,:,1)+(:,:,2)+(:,:,3)
    bb8 = unit8 (bb*255);
    db=demosaic(bb8, 'grgb');
    imshow(db)
    l8=unit8(lena_std*255);
    imshow(db, l8);
```