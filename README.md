# Digital-Signal-Processing--FIR-HIGH-PASS-FILTER-DESIGN
## AIM:
To generate design of High pass FIR digital filter using Window.

## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the hIGH Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
% Pradhagini A [212224050031]

clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc=input('enter the value of cut off frequency');
N=input('enter the value of filter');
alpha=(N-1)/2;
eps=0.001;
%High Pass Filter Coefficient
n=0:1:N-1;
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps))
%Hamming Window Sequence
n=0:1:N-1;
wh=0.54-0.46*cos((2*pi*n)/(N-1))
hn=hd.*wh
% Plot the High Pass Filter with Hamming Window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
<img width="1598" height="931" alt="image" src="https://github.com/user-attachments/assets/45673333-50e5-4c3c-8bac-22ae50d1c337" />

## RESULT:
<img width="1600" height="876" alt="image" src="https://github.com/user-attachments/assets/0f7eec20-3f56-457b-8816-142134454db0" />
