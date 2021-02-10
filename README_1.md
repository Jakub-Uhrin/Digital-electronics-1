# Digital-electronics-1
## DPC-DE1  2021
Jakub Uhrin 221457
### 01 Gates

1. Github link: https://github.com/Jakub-Uhrin/Digital-electronics-1

2. VLD Playground kód:
design:

*------------------------------------------------------------------------
*--Verification of De Morgan's laws of function
*------------------------------------------------------------------------
*
*library ieee;               -- Standard library
*use ieee.std_logic_1164.all;-- Package for data types and logic operations
*
*------------------------------------------------------------------------
*-- Entity declaration 
*------------------------------------------------------------------------
*entity gates is
*    port(
*        a_i    : in  std_logic;         -- Data input
*        b_i    : in  std_logic;         -- Data input
*        c_i	   : in  std_logic;
*       
*        f_o    : out std_logic; 
*        fnand_o: out std_logic;
*        fnor_o : out std_logic
*       
*   );
*end entity gates;
*
*------------------------------------------------------------------------
*-- Architecture body for basic gates
*------------------------------------------------------------------------
*architecture dataflow of gates is
*begin
*    f_o     <= ((not b_i) and a_i) or ((not c_i) and (not b_i));
*    fnand_o <= ((not b_i) nand a_i)nand((not c_i) nand (not b_i));
*   fnor_o  <= (b_i nor (not a_i)) or ( c_i nor b_i);
*
*end architecture dataflow;

Screenshot signálů:
![Screenshot](images/signals.png)

EDA link: https://www.edaplayground.com/x/rvjS
