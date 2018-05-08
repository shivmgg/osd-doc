Programmer Interface: Data
--------------------------

The CDM-OR1K module generates only one type of event packets: breakpoint-hit packets.
Breakpoint-hit packets contain the data in the form of (id,value) tuples.

Breakpoint-hit Packets
^^^^^^^^^^^^^

A Breakpoint-hit Packet encapsulates a breakpoint event, which consists of an identifier ``id`` and an associated value (breakpoint address/value) ``value``.

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
    - ``id``

  * - 1
    - ``value[15:0]``

  * - 2
    - ``value[31:16]``




