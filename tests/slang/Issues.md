# Remaining Slang failures

## Unknown Modules

- asic/techmap/techmap_chtype.ys: <inlined>:15: ERROR: unknown module '_TECHMAP_PLACEHOLDER_'
- asic/techmap/cellname.ys: <inlined>:4: ERROR: unknown module 'namedsub'
- asic/techmap/autopurge.ys: <inlined>:2: ERROR: unknown module 'foobar'
- fpga/xilinx/dsp_abc9.ys: <inlined>:2: ERROR: unknown module 'DSP48E1'
- fpga/xilinx/abc9_dff.ys: <inlined>:2: ERROR: unknown module 'FDRE'
- fpga/xilinx/xilinx_dsp.ys: <inlined>:2: ERROR: unknown module 'DSP48E1'
- fpga/ice40/ice40_wrapcarry.ys: <inlined>:2: ERROR: unknown module 'SB_CARRY'
- fpga/ice40/ice40_opt.ys: <inlined>:3: ERROR: unknown module '$__ICE40_CARRY_WRAPPER'

## Parameter Issues

- basic/verific/blackbox_empty.ys: <inlined>:2: ERROR: parameter 'PATH' does not exist in 'TEST_CELL' [-Wundefined-param-override]
- basic/various/bug3462.ys: <inlined>:4: ERROR: parameter 'd' does not exist in 'sub' [-Wundefined-param-override]

## Syntax

- asic/techmap/bug2972.ys: <inlined>:2: ERROR: expected identifier
- asic/techmap/dfflibmap_formal.ys: <inlined>:4: ERROR: expected member
- asic/techmap/dlatchlibmap_formal.ys: <inlined>:4: ERROR: expected member
- asic/techmap/techmap_replace.ys: <inlined>:2: ERROR: unknown module 'foobar'
- asic/techmap/cellmatch.ys: <inlined>:3: ERROR: only 'output' variable port declarations may have an initializer expression
- asic/techmap/bug2183.ys: <inlined>:5: ERROR: expression is not assignable
- basic/various/rand_const.ys: rand_const.sv:2: ERROR: member not allowed in module declaration
- basic/various/box_derive.ys: <inlined>:2: ERROR: use of undeclared identifier 'X'
- basic/various/struct_access.ys: struct_access.sv:24: ERROR: invalid member access for type 'logic[1:0]'
- fpga/xilinx/xilinx_srl_enable.ys: <inlined>:9: ERROR: expected identifier

## Hierarchy

- asic/abc_new/paramod_equiv.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 2: top/t:$paramod*
- asic/techmap/iopadmap.ys: ERROR: Module `\ibuf' referenced in module `\a' in cell `$iopadmap$a.i' is not part of the design.
- asic/techmap/clkbufmap.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 3: top/t:clkbuf
- asic/techmap/module_not_derived.ys: ERROR: Assertion failed: selection is empty: t:mycell a:module_not_derived %i
- basic/opt/bug1793.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 2: sub/o:*
- basic/various/rename_scramble_name.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 1: c:$_*_
- basic/various/rename_unescape.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 1: w:$e

## Metadata

- basic/verific/port_bus_order.ys: ERROR: Shell command returned error code 256.
- basic/verific/enum_values.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 1: top/state a:wiretype=\state_t %i
- basic/verilog/sbvector.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 1: w:i1 a:single_bit_vector %i
- basic/various/check_nolatches.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 1: t:$dlatch a:always_latch %i
- basic/various/json_netnames_signed.ys: ERROR: Shell command returned error code 256.
- basic/various/splitnets.ys: ERROR: Assertion failed: selection contains 1 elements instead of the asserted 0: w:a

## Optimization

- basic/peepopt/muldiv_c.ys: ERROR: Assertion failed: selection is not empty: t:$div
- basic/proc/yosys_latch.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 2: t:$adlatch
- basic/proc/proc_latches.ys: ERROR: Expected warning pattern 'Latch inferred for signal' not found !
- basic/opt/opt_expr_alu.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 1: t:$pos
- basic/opt/opt_expr.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 1: t:$add r:A_WIDTH=5 r:B_WIDTH=4 r:Y_WIDTH=5 %i %i %i
- basic/various/mem2reg.ys: ERROR: Assertion failed: selection contains 0 elements instead of the asserted 1: m:data1 a:src=<inlined>:4.43-4.48 %i
- fpga/xilinx/dsp_cascade.ys: ERROR: Assertion failed: selection contains 10 elements instead of the asserted 5: t:FDRE

## Specify / Timing

- asic/techmap/xaiger2-keep-box.ys: ERROR: Module 'box' with (* abc9_box *) has no timing (and thus no connectivity) information.
- asic/techmap/xaiger2-5169.ys: ERROR: Module 'CC_MX4' with (* abc9_box *) has no timing (and thus no connectivity) information.
- fpga/xilinx/bug1605.ys: ../../../../techlibs/xilinx/cells_sim.v:509: ERROR: cannot refer to 'IS_C_INVERTED' in state-dependent path condition expression; only locally defined nets and variables are allowed
- fpga/ecp5/abc9_inout_pad_input.ys: ../../../../techlibs/lattice/common_sim.vh:304: ERROR: cannot refer to 'SRMODE' in state-dependent path condition expression; only locally defined nets and variables are allowed

## Slang Semantics

- basic/various/submod.ys: Warning: Drivers conflicting with a constant 1'x driver: module input a[0], ERROR: Found 1 problems in 'check -assert'.

### Multiple Async Loads

- asic/abc_new/openroad/dffrsn_equiv.ys: <inlined>:6: ERROR: multiple asynchronous loads unsupported

## SAT Errors

- basic/opt/pow_assoc.ys: ERROR: Found 2 unproven $equiv cells in 'equiv_status -assert'.
- basic/opt/opt_dff_dffmux.ys: ERROR: Found 1 unproven $equiv cells in 'equiv_status -assert'.
- basic/various/dynamic_part_select.ys: ERROR: Called with -verify and proof did fail!
