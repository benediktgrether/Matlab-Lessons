# Matlab Übungen 03

> ** a.) Schreiben Sie eine Funktion, welche das Pixelkoordinatensystem
> einer Bildmatrix in das kartesische Koordinatensystem umwandelt
>


> Um in Matlab diese Funktion schreiben zu können muss man auf 
> + new -> function 
``` Matlab
function out = my_affin(in)
%Affine Transformation
[Z,S,C] = size(in);
%out = in;
% oder 
out = uint8(zeros(Z,S,C));
for z = 1:Z
    for s = 1:S
    x1 = z;
    y1 = s;
    %x2 = a1 * x1 + a2 * y1 + x0;
    %y2 = b1 * x1 + b2 * y1 + y0;
    
     x2 = 2 * x1 + 0 * y1 + 0;
     y2 = 0 * x1 + 2 * y1 + 0;
        if(x2 <= 512) && (x2 >= 1) && (y2 <= 512) && (y2 >= 1)
            for c = 1:C
                out (x1,y1,c) = in(round(x2), round(y2),c);
            end
        end
    end 
end
``` 
