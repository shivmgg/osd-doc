Core Debug Module for OpenRISC CPU Cores (CDM-OR1K)
===================================================

.. figure:: ../../img/debug_module_cdm_or1k.*
   :alt: High Level overview 
   :name: fig:debug_module_cdm

   High Level Overview 

The core debug module implements run-control debugging for OR1k CPU core. 
The module has a memory mapped interface. CDM-OR1K maps each 32-bit wide 
debug register of OR1K debug unit into two 16-bit wide OSD registers. 
The run-control debugger, i.e. GDB sends register access requests to the module through OSD debug network. 
The CDM-OR1K then transfers the corresponding data values from OSD specific 
registers to OR1K debug unit over the debugging signals specified in :doc:`System Interface <systemif>`. 
In case of a debug event (CPU debug stall event), ``interrupt`` signals are asserted. 
As a reaction, the module reads a defined address and 
the core-specific part of the CDM-OR1K generates a debug event.



.. toctree::
   :maxdepth: 1

   systemif
   dbgregisters
   datainterface

