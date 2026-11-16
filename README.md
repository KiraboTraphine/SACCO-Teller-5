# SACCO Teller-5 System

## Project Overview
This project demonstrates a digital teller-call system for a Savings and Credit Cooperative Organisation (SACCO) in Masaka, Uganda.

The system uses priority encoder logic and a seven-segment display to identify which teller is calling the next customer.

## Project Objectives
- Design a priority encoder for teller-call requests.
- Give priority to the highest-numbered teller when multiple buttons are pressed.
- Generate binary output signals for teller selection.
- Use a valid signal (V) to identify active requests.
- Display the selected teller number using a seven-segment display.

## Software Used
- Hneemann Digital
- GitHub

## Project Files
- `SACCO_5_Tellers.dig` — Digital circuit file.

## How to Open the Circuit
1. Download the `.dig` file from this repository.
2. Open Hneemann Digital.
3. Open the downloaded circuit using **File → Open**.
4. Start the simulation.
5. Toggle the teller input buttons and observe the outputs.

## Circuit Development
The original design uses four teller inputs (R1–R4), with R4 having the highest priority.

The proposed extension adds R5 for mobile money services. Supporting five tellers requires three encoder output bits (Y2, Y1 and Y0) instead of two.

The new priority order is:

**R5 > R4 > R3 > R2 > R1**

## Expected Digit 5 Output
The seven-segment display must activate segments **a, c, d, f and g** to show digit 5.

The expected output pattern is:

`a=1, b=0, c=1, d=1, e=0, f=1, g=1`

## Testing
The original four-teller design was tested using all 16 combinations of R1–R4, and the test passed successfully.

The five-teller extension requires separate simulation and verification.

## Conclusion
This project demonstrates how priority encoders and seven-segment decoders can be applied to a SACCO teller-call system. It also explores how the existing design can be extended to accommodate a fifth counter.
