<img width="790" height="582" alt="image" src="https://github.com/user-attachments/assets/968ab112-b8bb-4bcd-b562-06e6c1c7148d" /># Digital-Signal-Processing--FIR-BAND-PASS-FILTER-DESIGN
## AIM:
To generate design of Band Pass FIR digital filter using Window.
## Software Required:
MATLAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen 
clear all; % clear screen 
close all; % close all figure windows 
Wc1=input('enter the value of Wc1=');  
Wc2=input('enter the value of Wc2=');  
N=input('enter the value of N='); 
alpha=(N-1)/2;  
eps=0.001;  
%Band Pass Filter Coefficient 
n=0:1:N-1;  
hd=(sin(Wc1*(n-alpha+eps))-sin(Wc2*(n-alpha+eps)*pi))./((n-alpha+eps)*pi)  
%Hanning Window Sequence  
n=0:1:N-1;  
wh=0.5-0.5*cos((2*pi*n)/(N-1))  
hn=hd.*wh  
% Plot the Low Pass Filter with Hanning Window Technique 
w=0:0.01:pi;  
h=freqz(hn,1,w);  
plot(w/pi,abs(h),'ms');
```
## OUTPUT:
<img width="790" height="582" alt="image" src="https://github.com/user-attachments/assets/d77c58a0-a56b-4b5a-85b8-6bec45904c53" />


## RESULT:
![WhatsApp Image 2026-04-01 at 23 33 43](https://github.com/user-attachments/assets/aedbd41b-688d-4846-82d4-42952349d180)

