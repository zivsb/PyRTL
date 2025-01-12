Helper Functions
================

Cutting and Extending WireVectors
---------------------------------

The functions below provide ways of combining, slicing, and extending WireVectors in
ways that are often useful in hardware design.  The functions below extend those member
functions of the WireVector class iself (which provides support for the python builtin
``len``, slicing as just as in a python list e.g. ``wire[3:6]``, ``zero_extend``, ``sign_extend``,
and many operators such as addition and multiplication).  

.. autofunction:: pyrtl.corecircuits.concat
.. autofunction:: pyrtl.corecircuits.concat_list
.. autofunction:: pyrtl.corecircuits.match_bitwidth
.. autofunction:: pyrtl.helperfuncs.truncate
.. autofunction:: pyrtl.helperfuncs.chop

Coercion to WireVector
----------------------

In PyRTL there is only one function in charge of coercing values into WireVectors, and that is
``as_wires``.  This function is called in almost all helper functions and classes to manage 
the mixture of constants and WireVectors that naturally occur in hardware development.

.. autofunction:: pyrtl.corecircuits.as_wires

Control Flow Hardware
---------------------

.. autofunction:: pyrtl.corecircuits.mux
.. autofunction:: pyrtl.corecircuits.select
.. autofunction:: pyrtl.corecircuits.enum_mux
.. autofunction:: pyrtl.corecircuits.bitfield_update
.. autofunction:: pyrtl.corecircuits.bitfield_update_set
.. autofunction:: pyrtl.helperfuncs.match_bitpattern

Creating Lists of WireVectors
-----------------------------

.. autofunction:: pyrtl.helperfuncs.input_list
.. autofunction:: pyrtl.helperfuncs.output_list
.. autofunction:: pyrtl.helperfuncs.register_list
.. autofunction:: pyrtl.helperfuncs.wirevector_list

Interpreting Vectors of Bits
----------------------------

Under the hood, every single `value` a PyRTL design operates on is a bit vector (which is, in turn, simply 
an integer of bounded power-of-two size.  Interpreting these bit vectors as humans, and turning human
understandable values into their corresponding bit vectors, can both be a bit of a pain.  The functions
below do not create any hardware but rather help in the process of reasoning about bit vector representations
of human understandable values.

.. autofunction:: pyrtl.helperfuncs.val_to_signed_integer
.. autofunction:: pyrtl.helperfuncs.val_to_formatted_str
.. autofunction:: pyrtl.helperfuncs.formatted_str_to_val
.. autofunction:: pyrtl.helperfuncs.infer_val_and_bitwidth
.. autofunction:: pyrtl.helperfuncs.log2

Debugging
---------

.. autofunction:: pyrtl.core.set_debug_mode
.. autofunction:: pyrtl.helperfuncs.probe
.. autofunction:: pyrtl.helperfuncs.rtl_assert
.. autofunction:: pyrtl.helperfuncs.check_rtl_assertions
.. autofunction:: pyrtl.helperfuncs.find_loop
.. autofunction:: pyrtl.helperfuncs.find_and_print_loop

Reductions
----------

.. autofunction:: pyrtl.corecircuits.and_all_bits
.. autofunction:: pyrtl.corecircuits.or_all_bits
.. autofunction:: pyrtl.corecircuits.xor_all_bits
.. autofunction:: pyrtl.corecircuits.parity
.. autofunction:: pyrtl.corecircuits.rtl_any
.. autofunction:: pyrtl.corecircuits.rtl_all
.. autofunction:: pyrtl.corecircuits.tree_reduce

Extended Logic and Arithmetic
-----------------------------

The functions below provide ways of comparing and arithmetically combining WireVectors
in ways that are often useful in hardware design.  The functions below extend those member
functions of the WireVector class iself (which provides support for addition, unsigned
multiplication, unsigned comparison, and many others).  

.. autofunction:: pyrtl.corecircuits.signed_add
.. autofunction:: pyrtl.corecircuits.signed_mult
.. autofunction:: pyrtl.corecircuits.signed_lt
.. autofunction:: pyrtl.corecircuits.signed_le
.. autofunction:: pyrtl.corecircuits.signed_gt
.. autofunction:: pyrtl.corecircuits.signed_ge
.. autofunction:: pyrtl.corecircuits.shift_left_arithmetic
.. autofunction:: pyrtl.corecircuits.shift_right_arithmetic
.. autofunction:: pyrtl.corecircuits.shift_left_logical
.. autofunction:: pyrtl.corecircuits.shift_right_logical
