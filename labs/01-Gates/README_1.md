# Digital-electronics-1
## DPC-DE1  2021
Jakub Uhrin 221457
### 01 Gates

####1. 

Github link: https://github.com/Jakub-Uhrin/Digital-electronics-1

####2. 

| c | b | a | f |
|---|---|---|---|
| 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 0 |



VLD Playground kód:

design:
```
------------------------------------------------------------------------
--Verification of De Morgan's laws of function
------------------------------------------------------------------------

library ieee;               -- Standard library
use ieee.std_logic_1164.all;-- Package for data types and logic operations

------------------------------------------------------------------------
-- Entity declaration 
------------------------------------------------------------------------
entity gates is
    port(
        a_i    : in  std_logic;         -- Data input
        b_i    : in  std_logic;         -- Data input
        c_i	   : in  std_logic;
       
        f_o    : out std_logic; 
        fnand_o: out std_logic;
        fnor_o : out std_logic
       
   );
end entity gates;

------------------------------------------------------------------------
-- Architecture body for basic gates
------------------------------------------------------------------------
architecture dataflow of gates is
begin
    f_o     <= ((not b_i) and a_i) or ((not c_i) and (not b_i));
    fnand_o <= ((not b_i) nand a_i)nand((not c_i) nand (not b_i));
    fnor_o  <= (b_i nor (not a_i)) or ( c_i nor b_i);

end architecture dataflow;
```


Screenshot signálů:

![Screenshot](images/signals.png)

EDA Playgrounds link: https://www.edaplayground.com/x/rvjS

####3.

VLD Playground kód:

design:
```
------------------------------------------------------------------------
--Verification of De Morgan's laws and Verification of Distributive laws
------------------------------------------------------------------------

library ieee;               -- Standard library
use ieee.std_logic_1164.all;-- Package for data types and logic operations

------------------------------------------------------------------------
-- Entity declaration for basic gates
------------------------------------------------------------------------
entity gates is
    port(
        x_i   : in  std_logic;         -- Data input
        y_i   : in  std_logic;        
        z_i	  : in  std_logic;
       
        f11_o    : out std_logic; 
        f12_o    : out std_logic;
        f13_o    : out std_logic;
        f14_o    : out std_logic;
        f21_o    : out std_logic;
        f22_o    : out std_logic;
        f31_o	 : out std_logic;
        f32_o	 : out std_logic
    );
end entity gates;

------------------------------------------------------------------------
-- Architecture body 
------------------------------------------------------------------------
architecture dataflow of gates is
begin
    f11_o   <= x_i and (not x_i);
    f12_o   <= x_i or (not x_i);
    f13_o   <= x_i or x_i or x_i;
    f14_o   <= x_i and x_i and X_i;
    f21_o   <= (x_i and y_i) or (x_i and z_i);
    f22_o   <= (x_i and (y_i or z_i));
    f31_o   <= (x_i or y_i) and (x_i or z_i);
    f32_o   <= (x_i or (y_i and z_i));

end architecture dataflow;
```

Screenshoty signálů:

![Screenshot](images/signály_x.png)

![Screenshot](images/signály_dis.png)

odkaz na VLD Playground: https://www.edaplayground.com/x/YXyk
