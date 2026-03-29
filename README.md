# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
~~~
close all; % close all figure windows 
wc=input('enter the value of cut off frequency');  
N=input('enter the value of filter');  
alpha=(N-1)/2;  
eps=0.001;  
%Low Pass Filter Coefficient 
n=0:1:N-1;  
hd=sin(wc*(n-alpha+eps))./(pi*(n-alpha+eps)) 
%Hanning Window Sequence  
n=0:1:N-1;  
wh=0.5-0.5*cos((2*pi*n)/(N-1)) 
hn=hd.*wh  
% Plot the low Pass Filter with Hanning Window Technique 
w=0:0.01:pi;  
h=freqz(hn,1,w); 
plot(w/pi,abs(h),'ms');
~~~

## OUTPUT:
![dspexpo3](https://github.com/user-attachments/assets/6296a900-5706-4d85-bde9-3ff6e0441b78)


## RESULT:

![result4](https://github.com/user-attachments/assets/0e010638-c202-4e23-9681-1d713fdd515e)
