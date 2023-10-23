# Reverse Engineering Challenges List
****
## Challenge 1 (Hidden)
  - **Category**: Reverse Engineering
  - **Description**: An elf executable which the player have to reverse eng. to get the flag.
  - **Flag**: Genctf{Y0u_g0t_hidd3n_flag}
  - **Quick Guide**: Use a debugger like cutter or IDA for the file. The executable will deofucate and print the flag only if a variable ```input``` has a certain value which is **layered** (the player has to find this though investigation), so set a breakpoint when input variable is compared to variable ```key```; and populate the value of variable ```input``` with layered.


by Gurkirat
