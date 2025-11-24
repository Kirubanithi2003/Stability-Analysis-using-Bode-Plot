# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![cs71](https://github.com/user-attachments/assets/6e470b95-68f5-4b16-9778-d2a266eded3d)
![cs72](https://github.com/user-attachments/assets/11e220fc-2267-49c5-9b1b-b6b8fb79f398)
![cs73](https://github.com/user-attachments/assets/d7582271-f911-40be-b5c7-1da51b80d4fa)
## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num = [1];
den = [0.05 0.6 1  0];
sys = tf(num,den)
bode(sys)
grid on;
[Gm Pm Wpc Wgc] = margin(sys)
GmindB = 20*iog10(Gm)
if (wpc > wgc)
    disp('stable')
elseif (Wpc == Wgc)
    disp('marginally stable')
else ('unstable')
end
```
## Output:
<img width="1722" height="999" alt="Screenshot 2025-11-16 232337" src="https://github.com/user-attachments/assets/efe9d7b8-bc86-4df9-9a89-264a6e7a51d8" />
## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 6.7082 (16.5330 dB)
Phase Margin = 16.2940 deg Gain
Gain crossover frequency = 0.8710 rad/s
Phase crossover frequency = 4.4721 rad/s
The system is stable
