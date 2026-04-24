week-10

# Complete Quick Revision Sheet: DAC & ADC (Answer Any Typical Exam Question)

---

# 1. D/A Converter (DAC)

## Definition

Converts **digital binary input** into equivalent **analog voltage/current output**.

---

# Types of DAC

## 1. Binary Weighted Resistor DAC

Uses resistors weighted as:

R,2R,4R,8R,16R...

### Important:

For n-bit DAC:

* MSB resistor = (R)
* LSB resistor = (2^{n-1}R)

### Example:

5-bit DAC, MSB resistor = 10kΩ

R_{LSB}=2^{4}\times10k=160k\Omega

---

## 2. R-2R Ladder DAC

Uses only two resistor values:

R\ and\ 2R

### Number of resistors:

For n-bit DAC:

* R resistors = n
* 2R resistors = n + 1

Example:

8-bit DAC → 9 resistors of 2R

---

# Resolution of DAC

Smallest output step change.

## Formula:

\text{Resolution}=\frac{1}{2^n-1}\times100%

(Used in many exams)

### Examples:

6-bit DAC:

\frac{100}{63}=1.59%

7-bit DAC:

\frac{100}{127}=0.787%

---

# Output Voltage of DAC

## General Formula:

V_o=V_{ref}\left(\frac{D}{2^n}\right)

Where:

* D = decimal value of binary input

Example:

4-bit DAC input = 1010 = 10

V_o=5\left(\frac{10}{16}\right)=3.125V

---

# R-2R Ladder Bit Weights

For 4-bit:

* MSB = 1/2
* Next = 1/4
* Next = 1/8
* LSB = 1/16

Example:
Only D₂ = 5V ON

V_o=5\times\frac14=1.25V

---

---

# 2. A/D Converter (ADC)

## Definition

Converts analog input into digital output.

---

# Types of ADC

---

## 1. Flash ADC

Fastest ADC.

Uses many comparators.

### Formula:

Comparators=2^n-1

Examples:

8-bit:

255

4-bit:

15

---

## 2. Counter Type ADC

Uses counter + DAC + comparator.

### Worst Case Conversion Time:

2^n-1\ clock\ cycles

Sometimes written as:

2^n

Example:

12-bit:

4095 or 4096 cycles

---

## 3. Tracking ADC

Improved counter ADC.

### Best for:

✅ Slowly varying signals

Because it tracks previous value.

---

## 4. Successive Approximation ADC (SAR)

Most common.

### Conversion time:

n\ clock\ cycles

Example:

24-bit = 24 cycles

---

# Speed Comparison

Flash > SAR > Tracking > Counter

---

# Cost Comparison

Counter < Tracking < SAR < Flash

---

# Accuracy Comparison

SAR\ is\ widely\ preferred

---

# ADC Resolution

For n-bit ADC:

Resolution=\frac{V_{FS}}{2^n-1}

Where (V_{FS})= Full scale voltage

Example:

7-bit ADC, 10V full scale

\frac{10}{127}=0.0787V

Percentage:

0.787%

---

# Most Repeated Exam Questions

## DAC

### 1. Number of steps:

2^n

### 2. Resolution:

\frac{1}{2^n-1}\times100

### 3. Binary weighted LSB resistor:

2^{n-1}R

### 4. Flash ADC comparators:

2^n-1

### 5. Counter ADC cycles:

2^n-1

### 6. SAR cycles:

n

---

# Shortcut Tricks

## If asked "Slowly varying signal?"

✅ Tracking ADC

## If asked "Fastest ADC?"

✅ Flash ADC

## If asked "Most economical?"

✅ Counter ADC

## If asked "Best balance speed + accuracy?"

✅ SAR ADC

## If asked "Only two resistor values?"

✅ R-2R DAC

---

# Final Memory Table

| Topic                     | Formula  |
| ------------------------- | -------- |
| Resolution                | 1/(2ⁿ−1) |
| Flash comparators         | 2ⁿ−1     |
| Counter ADC cycles        | 2ⁿ−1     |
| SAR cycles                | n        |
| Weighted DAC LSB resistor | 2ⁿ⁻¹R    |
| R-2R 2R resistors         | n+1      |

---

# If you study only this sheet, you can solve 95% DAC/ADC MCQs.
