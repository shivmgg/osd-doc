Core Debug Module (CDM-OR1K)
=======================

.. figure:: ../../img/debug_module_cdm.*
   :alt: Core Debug Module
   :name: fig:debug_module_cdm

   Core Debug Module

The core debug module implements run-control debugging for or1k 
core. The implementation is to a certain degree core-dependent, but a
generic implementation is sketched in @fig:debug\_module\_cdm. It has a
memory mapped interface as described above. The debug control, status
information and core registers are mapped in memory regions. The
run-control debugger, i.e. GDB then sends register access requests. In
case of a debug event (Breakpoint-hit) ``interrupt`` signals are
asserted. As a reaction the CDM-OR1K reads a defined address and the
core-specific part of the CDM-OR1K generates a debug event.

In the current implementation, the 32 bit debug registers of or1k are mapped into two 16 bit wide OSD registers.

.. toctree::
   :maxdepth: 1

   systemif
   dbgregisters
   datainterface

