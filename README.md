# Smart-Digital-Lock-System-VHDL
Design and implementation of a Smart Digital Lock System using VHDL with keypad and 7-segment display.
9:21â€¯AM
smart_lock_top.vhd
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity smart_lock_top is
    Port (
        clk : in STD_LOGIC;
        reset : in STD_LOGIC;
        keypad : in STD_LOGIC_VECTOR(3 downto 0);
        unlock : out STD_LOGIC;
        seg : out STD_LOGIC_VECTOR(6 downto 0)
    );
end smart_lock_top;

architecture Behavioral of smart_lock_top is
begin
    unlock <= '1' when keypad = "1010" else '0';
end Behavioral;