# 02-Logic
## 1.
|Dec. equvivalent|B[1:0]|A[1:0]|B is grater than A|B equals A|B is less than A|
|----------------|------|------|------------------|----------|----------------|
|0|00|00|0|1|0|
|1|00|01|0|0|1|
|2|00|10|0|0|1|
|3|00|11|0|0|1|
|4|01|00|1|0|0|
|5|01|01|0|1|0|
|6|01|10|0|0|1|
|7|01|11|0|0|1|
|8|10|00|1|0|0|
|9|10|01|1|0|0|
|10|10|10|0|1|0|
|11|10|11|1|0|0|
|12|11|00|1|0|0|
|13|11|01|1|0|0|
|14|11|10|1|0|0|
|15|11|11|0|1|0|

## 2.

![alt text](https://github.com/Jakub-Uhrin/Digital-electronics-1/blob/main/images/MapBeqA.png "VMapBeqA")
             
![alt text](https://github.com/Jakub-Uhrin/Digital-electronics-1/blob/main/images/MapBlessA.png "VMapBlessA")
             
![alt text](https://github.com/Jakub-Uhrin/Digital-electronics-1/blob/main/images/MapBgrA.png "VMapBgrA")

![alt text](https://github.com/Jakub-Uhrin/Digital-electronics-1/blob/main/images/mapsEQ.png "Map Equations")

```
------------------------------------------------------------------------
--
-- Example of 4-bit binary comparator using the when/else assignment.
-- EDA Playground
--
-- Dept. of Radio Electronics, Brno University of Technology, Czechia
-- This work is licensed under the terms of the MIT license.
--
------------------------------------------------------------------------
 
library ieee;
use ieee.std_logic_1164.all;
 
------------------------------------------------------------------------
-- Entity declaration for 4-bit binary comparator
------------------------------------------------------------------------
entity comparator_2bit is
    port(
        a_i           : in  std_logic_vector(4 - 1 downto 0);
        b_i			  :	in  std_logic_vector(4 - 1 downto 0);
 
 
        -- COMPLETE ENTITY DECLARATION
 
 
        B_less_A_o    : out std_logic ;      -- B is less than A
        B_equals_A_o  : out std_logic ;
        B_greater_A_o : out std_logic
    );
end entity comparator_2bit;
 
------------------------------------------------------------------------
-- Architecture body for 2-bit binary comparator
------------------------------------------------------------------------
architecture Behavioral of comparator_2bit is
begin
    B_greater_A_o <= '1' when (b_i > a_i) else '0';
    B_equals_A_o  <= '1' when (b_i = a_i) else '0';
    B_less_A_o    <= '1' when (b_i < a_i) else '0';
 
 
    -- WRITE "EQUALS" AND "LESS" ASSIGNMENTS HERE
 
 
end architecture Behavioral;
```
