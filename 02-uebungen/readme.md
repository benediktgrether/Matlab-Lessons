# Matlab Übungen 02

> **a) Geben Sie die Transformationsmatrix des HSI-Farbmodells ein**

``` Matlab
>> HSI = [2/sqrt(6) 0 1/sqrt(3);
-1/sqrt(6) 1/sqrt(2) 1/sqrt(3);
-1/sqrt(6) -1/sqrt(2) 1/sqrt(3)]
 
``` 
>Ergebnis
``` Matlab
HSI =

    0.8165         0    0.5774
   -0.4082    0.7071    0.5774
   -0.4082   -0.7071    0.5774


   %Transformierte Matrix 
   HSI' 

   ans =

    0.8165   -0.4082   -0.4082
         0    0.7071   -0.7071
    0.5774    0.5774    0.5774
 
    HSI * HSI'

    ans =

        1.0000         0         0
            0    1.0000    0.0000
            0    0.0000    1.0000

``` 

> **c) Schreiben Sie eine Funktion, welche ein RGB-Bild in ein HSI-Bild
umwandelt**

``` Matlab
>> hsv = rgb2hsv(lena_std);
>> imshow(hsv)
```

``` Matlab
>> r=lena_std(:,:,1);
>> g=lena_std(:,:,2);
>> b=lena_std(:,:,3);
>> rgb = [r(:),g(:),b(:)];
```

> **h) Wenden Sie die Funktion rgb2gray in Matlab auf lena_std an**
```Matlba
lena_grey = rgb2gray(lena_std);
>> imshow(lena_grey)
```