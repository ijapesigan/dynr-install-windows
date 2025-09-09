# Installing the **dynr** R Package on Windows

## 1. Install R
- Download R for Windows from:  
  <https://cloud.r-project.org/bin/windows/base/R-4.5.1-win.exe>  
- Double-click the installer `R-4.5.1-win.exe`.  
- If you do not have administrative privileges, install R to:  
  `C:\Users\USERNAME\AppData\Local\Programs\R\R-4.5.1`

## 2. Install Rtools
- Download Rtools for Windows from:  
  <https://cloud.r-project.org/bin/windows/Rtools/rtools45/files/rtools45-6608-6492.exe>  
- Double-click the installer `rtools45-6608-6492.exe`.  
- Without administrative privileges, install Rtools to:  
  `C:\Users\USERNAME\rtools45`

## 3. Add Rtools to the Path
1. Click the Windows button, type, and open **“Edit environment variables for your account.”**  
2. Select `Path` → **Edit…** → **New** and add:
   - `C:\Users\USERNAME\AppData\Local\Programs\R\R-4.5.1\bin`
   - `C:\Users\USERNAME\rtools45\ucrt64\bin`
   - `C:\Users\USERNAME\rtools45\x86_64-w64-mingw32.static.posix\bin`
3. Create new environment variables:
   - `LIB_GSL` = `C:\Users\USERNAME\rtools45\x86_64-w64-mingw32.static.posix\include\gsl`
   - `RTOOLS45_HOME` = `C:\Users\USERNAME\rtools45`

## 4. Install the dynr Package
- In R, run:  
  ```r
  install.packages("dynr")
- Test the installation with:
  ```r
  source("https://raw.githubusercontent.com/ijapesigan/dynr-install-windows/refs/heads/main/dynr-demo.R")
- A sucessful installation with output the following:
  ```r
  Coefficients:
           Estimate Std. Error t value ci.lower ci.upper Pr(>|t|)    
  spring   -0.10000    0.01583  -6.318 -0.13102 -0.06898   <2e-16 ***
  friction -0.20000    0.03598  -5.558 -0.27053 -0.12947   <2e-16 ***
  dnoise    1.00000    0.15505   6.450  0.69611  1.30389   <2e-16 ***
  mnoise    1.50000    0.08875  16.901  1.32605  1.67395   <2e-16 ***
  inipos    0.00000    1.37080   0.000 -2.68671  2.68671      0.5    
  ---
  Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

  -2 log-likelihood value at convergence = 4214.13
  AIC = 4224.13
  BIC = 4248.67

