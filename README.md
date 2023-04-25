# MineTest Logs
Welcome to my GitHub repository featuring the work logs of my contribution to the "Mine Test" project, a C++ based Minecraft recreation. This repository contains detailed accounts of my development process, including the creation of mods and other game assests for my Computer Engineering Design 1 Capstone Course (CEN3907C).
# Log Summary
3/27/2023 - Setup build (incomplete); Meeting with Blanchard

3/28/2023 - First build working; Team Meeting 3-6

3/29/2023 - Create test mod and upload video detailing processes
https://www.youtube.com/watch?v=3t5wI_HqaYs&ab_channel=SeanFerguson

4/10/2023 - Meetings discussing final presentation

4/11/2023 - Meeting with Matthew and Lisa to discuss Lua conversion class; Start work on testing Lua function

4/15/2023 - Picked rollback function as a start function to convert; Created l_native and n_ functions for rollback

4/16/2023 - Starting testing Get_Node_Actions

4/17/2023 - Finished testing for both Get_Node_Actions and Revert_Actions_By
# Bugs/Issues
- (FIXED)Can't convert complex data tpyes in C++ to Lua local variables.
  - Found what their equivilancies were by asking other group members. 
- (FIXED)Comparison of Lua and Native Get_Node_Actions Lua tables returning false although the command line returns are virtually the same.
  - Fix: Couldn't compare Lua Table items directly, rather set boolean and interate through.
- (FIXED)Get_Node_Actions returning a nill list.
  - Vector was the location of the currntly being tested block and time is how long it is being compared to. 
- (FIXED)Revert_Actions_By stating that I can't access static member function in code although no parameters are changed. Could be the fact that the log file gets passed as a reference in the file but rather passed statically by the l_native function. 
  - Fix: Missing header file include
- Comparing the native and lua Revert_Actions_By functions returns false although their command line outputs are the same. I believe this is comparing the metadata of the log file associated with the Revert Actions as the comparison is a deep comparison versus a shallow one.
