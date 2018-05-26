Core Debug Module (CDM)
=======================

.. figure:: ../../img/debug_module_cdm_overview.*
   :alt: High Level overview 
   :name: fig:debug_module_cdm

   High Level Overview 

The core debug module implements run-control debugging for the CPU core. 
The module has a memory mapped interface. CDM maps each Special-Purpose Register of the CPU core into CDM address spaces as described above.  
The run-control debugger, i.e. GDB sends register access requests to the module through OSD debug network. 
The module then transfers the corresponding data values from OSD specific registers to the CPU core over the debugging signals specified in :doc:`System Interface <systemif>`. 
The System Interface is designed to connect to an OR1K processor and other CPU cores having same debug ports.
 

In case of a debug event (CPU debug stall event), the CPU stalls and the control passes to GDB. 
The module reads/writes a defined address as per the request made by GDB.


.. toctree::
   :maxdepth: 1

   systemif
   dbgregisters
   datainterface

