# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-19 at 11 19 54](https://github.com/user-attachments/assets/487a4619-f224-4e15-b819-7ae659e4f6c0)
![WhatsApp Image 2025-11-19 at 11 19 56](https://github.com/user-attachments/assets/0f801a5d-b0c6-46f6-933b-75359b7a4d4c)
![WhatsApp Image 2025-11-19 at 11 19 57](https://github.com/user-attachments/assets/0f4492cc-6946-48a2-bed0-fe168222bf1d)
![WhatsApp Image 2025-11-19 at 11 19 58](https://github.com/user-attachments/assets/6c6cb8fb-dc08-4231-a7e4-00136bcfa771)

## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=[1];
den=[0.05 0.6 1 0];
sys=tf(num,den)
bode(sys)
grid on;
[gm pm wpc wgc]=margin(sys)
gmindb=20*log10(gm)
if(wpc>wgc)
    disp('stable')
elseif(wpc==wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```


## Output:
<img width="1920" height="1080" alt="CS EXP5" src="https://github.com/user-attachments/assets/a0f60270-4bf9-4fe6-8ea9-1d6efffa2fb2" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 40db <br>
Phase Margin =  70 degree<br>
Gain crossover frequency = 1 rad/sec<br>
Phase crossover frequency = 20 rad/sec<br>
The system is  ------------
