Two assertions from the written assertions were failed in the verilog file.

The labels for these two failed assertions in the verilog code are AST_T5, AST_OP8.

Bug 1: In line 42, the count40 is assigned to value 15 and the state changed to rdc_low. But , according to the specification sheet, when the count40 is 17, the state should change to rdc_low. So, the assertion AST_T5 was failed.

Bug 2: In line 96, trst is assigned to value 1 when in end_frame state. According to the specification sheet, trst should be 0 when in end_frame state. So, the assertions AST_OP8 was failed.

Also, AST_T5 and AST_T6 are related. Since count40 is assigned to value 15 instead of 17, the cover point at AST_T6 didn't get hit. Once the bug is fixed, the cover point at AST_T6 got hit.
