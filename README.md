
### AIM: 
To perform and verify multirate DSP without function using SCILAB. 

### APPARATUS REQUIRED: 
PC installed with SCILAB. 

### PROGRAM : 
```
clear; 
clc; 
close; 
n = 0:%pi/50:2*%pi; 
x = sin(%pi*n); //original signal 
M=input('Enter the downsampling factor'); 
L=input('Enter the upsampling factor'); 
//Down Sampling 
downsampling_x = x(1:M:length(x)); 
disp(x,'Input signal x(n)='); 
disp(downsampling_x,'Downsampled Signal'); 
figure(1); 
subplot(2,1,1) 
plot2d3(1:length(x),x); 
xtitle('original singal') 
subplot(2,1,2) 
plot2d3(1:length(downsampling_x),downsampling_x); 
xtitle('Downsampled Signal by a factor of M'); 
//Upsampling 
upsampling_x=[]; 
for i=1:length(x) 
upsampling_x(1,L*i)=x(i); 
end 
disp(x,'Input signal x(n)='); 
disp(upsampling_x,'Upsampled Signal');
figure(2); 
subplot(2,1,1); 
plot2d3(x); 
title('original signal'); 
subplot(2,1,2); 
plot2d3(upsampling_x); 
title('Upsampled Signal by a factor of L');
```
### OUTPUT: 

<img width="1298" height="230" alt="Screenshot 2025-11-10 153652" src="https://github.com/user-attachments/assets/9e4b7768-71e4-4ee1-b733-da57005de949" />

<img width="1920" height="1080" alt="Screenshot (164)" src="https://github.com/user-attachments/assets/4215a6cf-69ca-41e7-bd92-940cb1b97af6" />

<img width="1920" height="1080" alt="Screenshot (165)" src="https://github.com/user-attachments/assets/a5f16cb0-6cae-4f54-8a3c-eeaad73b297d" />


### RESULT: 
Thus the decimation process by a factor M and interpolation process by a factor L using 
SCILAB was implemented. 
