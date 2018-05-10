Programmer Interface: Data
--------------------------

The CDM-OR1K module generates only one type of event packets: CPU debug stall packets. Whenever the program counter in the CPU core matches with the watchpoint/breakpoint address, CPU is stalled and this event packet is generated. It notifies the debugger, i.e. GDB about a breakpoint or watchpoint hit.  
These packets contain the data in the form of ``reason`` payload word.

CPU Debug Stall packet
^^^^^^^^^^^^^^^^^^^^^^

A CPU Debug Stall Packet encapsulates a breakpoint or watchpoint event. 
The following fields in the header of the DI packet are set:

- ``FLAGS.TYPE`` is set to ``EVENT``
- ``FLAGS.TYPE_SUB`` is set to 0


.. tabularcolumns:: |p{\dimexpr 0.30\linewidth-2\tabcolsep}|p{\dimexpr 0.70\linewidth-2\tabcolsep}|
.. flat-table:: CDM-OR1K Packet Structure
  :widths: 3 7
  :header-rows: 1

  * - payload word
    - description

  * - 0
    - ``reason``: indicates the cause of event generation. 
	         

