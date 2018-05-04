Core Debug Module (CDM)
=======================

.. figure:: ../../img/debug_module_cdm.*
   :alt: Core Debug Module
   :name: fig:debug_module_cdm

   Core Debug Module

The core debug module implements run-control debugging for a processor
core. The implementation is to a certain degree core-dependent, but a
generic implementation is sketched in @fig:debug\_module\_cdm. It has a
memory mapped interface as described above. The debug control, status
information and core register are mapped in memory regions. The
run-control debugger (e.g., gdb) then sends register access requests. In
case of a debug event (breakpoint hit) ``interrupt`` signals are
asserted. As a reaction the CDM reads a defined address and the
core-specific part of the CDM generates a debug event.

In the current implementation, the 32 bit debug registers of or1k are mapped into 16 bit wide OSD registers.

.. toctree::
   :maxdepth: 1

   systemif
   dbgregisters


