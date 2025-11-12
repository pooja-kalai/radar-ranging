# Radar ranging
 
# Aim:
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.
# Theory:
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:
<img width="382" height="383" alt="image" src="https://github.com/user-attachments/assets/dd26abb6-5f06-4dc4-8c06-39eafb67831e" />




# Procedure:
1. Set Up the Python Environment: Ensure that Python is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice.

2. Import Necessary Libraries: Import the math library in Python.

3. Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.

4. Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power.

5. Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.

6. Execute the Program: Run the Python script to calculate and display the maximum range of the radar.





# program:
```
Pt = 500;
G = 500;
sigma = 1;
Ae = 10;

Smin = logspace(-12, -6, 100);
Rmax = ((Pt * G * sigma * Ae) ./ (16 * %pi^2 .* Smin)).^(1/4);
subplot(3,1,1);
plot(Smin, Rmax);

Ppeak = linspace(100, 10000, 100);
Rmax2 = ((Ppeak * G * sigma * Ae) ./ (16 * %pi^2 * 1e-5)).^(1/4);
subplot(3,1,2);
plot(Ppeak, Rmax2);

Gt = linspace(100, 2000, 100);
Rmax3 = ((Pt * Gt * sigma * Ae) ./ (16 * %pi^2 * 1e-5)).^(1/4);
subplot(3,1,3);
plot(Gt, Rmax3);
```

# output: 
 <img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/4cdab3a1-ca60-4c8c-9b30-a76601c2efe2" />

 # mannual calculation:
  ![WhatsApp Image 2025-11-12 at 23 08 37_210abf33](https://github.com/user-attachments/assets/a08fbfb0-aadb-4081-8968-e8aae31ce9cf)

# result:
Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Python program
