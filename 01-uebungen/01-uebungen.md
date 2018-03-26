# Matlab Übungen 01 

> **c.) Erzeugen Sie ein kleines Bild (z.B. 16x16) mit einem Bayer-Pattern**
>

## Code Matlab 
``` 

    b = zeros(16, 16, 3);
    
    % Farbe Rot
    b(1:2:end, 2:2:end, 1) = 1;

    % 1:2:end | 1 = erste Zeile , 2 = 2 Wert bis zum Ende.
    % 2:2:end | 2 = jede zweite Zeile , jeder 2 Wert bis zum Ende.
    % 1 | 1 Bekommt die Farbe Rot. 

    b(2:2:end, 1:2:end, 3) = 1;

    b(1:2:end, 1:2:end, 2) = 1;
    b(2:2:end, 2:2:end, 2) = 1;
    imtool(b)

```

> **d.) Wandeln Sie ein RGB-Farbbild in ein Bayer-Pattern-Bild um**
>

## Code Matlab 
``` 



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