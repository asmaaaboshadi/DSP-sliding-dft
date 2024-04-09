
clc;
clear;
X_N=[1 -4 3 8 2 7 3 5 1 8];
N=5;
k =[0:N-1];

X_1=X_N(1:N);
X_2=X_N(2:N+1);
X_3=X_N(3:N+2);
X_4=X_N(4:N+3);
X_5=X_N(5:N+4);
X_6=X_N(6:N+5);

XN=[X_1;X_2;X_3;X_4;X_1;X_6];

XK_1=fft(X_1);

ZforX_2=circshift(X_2,1);
XK_2=(XK_1(k+1)-X_1(1)+ZforX_2(1)).*exp(j*2*pi*k/N);

ZforX_3=circshift(X_3,1);
XK_3=(XK_2(k+1)-X_2(1)+ZforX_3(1)).*exp(j*2*pi*k/N);

ZforX_4=circshift(X_4,1);
XK_4=(XK_3(k+1)-X_3(1)+ZforX_4(1)).*exp(j*2*pi*k/N);

ZforX_5=circshift(X_5,1);
XK_5=(XK_4(k+1)-X_4(1)+ZforX_5(1)).*exp(j*2*pi*k/N);

ZforX_6=circshift(X_6,1);
XK_6=(XK_5(k+1)-X_5(1)+ZforX_6(1)).*exp(j*2*pi*k/N);

ZforX=[X_1;ZforX_2;ZforX_3;ZforX_4;ZforX_5;ZforX_6];
X_Z=[XK_1;XK_2;XK_3;XK_4;XK_5;XK_6];
FFT=[fft(X_1);fft(X_2);fft(X_3);fft(X_4);fft(X_5);fft(X_6)];

