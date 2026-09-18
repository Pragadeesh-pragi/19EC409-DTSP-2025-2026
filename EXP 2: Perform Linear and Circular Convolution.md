# EXP 1 : Linear and Circular Convolution

## AIM: 

 To perform Linear and Circular Convolution for two given sequence using SCILAB. 

## APPARATUS REQUIRED
PC installed with SCILAB

## PROGRAM:
## LINEAR CONVOLUTION
```sci
clc;
clear;
x = [1 1 1 1];
h = [1 2 3 4];
m = length(x);
n = length(h);
a=0:1:m-1;
b=0:1:n-1;
subplot(3,1,1);
plot2d3(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b,h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
for i = 1: n+m-1
    conv_sum = 0;
    for j = 1:i
        if (((i-j+1) <= n)&(j <=m))
            conv_sum = conv_sum + x(j)*h(i-j+1);
        end;
        y(i) = conv_sum;
    end;
end;
disp(y,'Convolution Sum using Direct Formula Method = ')
subplot(3,1,3);
plot2d3(y)
title('Graphical Representation of output Signal y');
```

### CALCULATIONS:

<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/52cf46da-494c-4303-accc-7c92d0ff2725" />
<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/bd857e8c-3eb7-4a07-b534-c6028d82d4f4" />

### SAMPLE OUTPUT:


<img width="610" height="460" alt="image" src="https://github.com/user-attachments/assets/4e07d380-0b95-4219-9984-e83d5e69275f" />



## RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
