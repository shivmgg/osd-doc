Programmer Interface: Control Registers
---------------------------------------

The Control Debug Module implements the :ref:`sec:spec:api:base_register_map`.

.. tabularcolumns:: |p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.40\linewidth-2\tabcolsep}|p{\dimexpr 0.20\linewidth-2\tabcolsep}|
.. flat-table:: CDM base register reset values
  :widths: 2 2 4 2
  :header-rows: 1

  * - address
    - name
    - description
    - reset value

  * - 0x0000
    - ``MOD_VENDOR``
    - module vendor
    - 0x0001

  * - 0x0001
    - ``MOD_TYPE``
    - module type identifier
    - 0x0006

  * - 0x0002
    - ``MOD_VERSION``
    - module version
    - 0x0000

  * - 0x0003
    - ``MOD_CS``
    - module control and status
    - 0x0000

  * - 0x0004
    - ``MOD_EVENT_DEST``
    - destination of debug events
    - 0x0000

Additionally, the CDM-OR1K module implements the following registers. 
Registers in the range **0x8000-0xFFFF** are forwarded to the corresponding special-purpose registers (SPRs) of the attached CPU core. 

.. tabularcolumns:: |p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.60\linewidth-2\tabcolsep}|
.. flat-table:: CDM register map
  :widths: 2 2 6
  :header-rows: 1

  * - address
    - name
    - description

  * - 0x0200
    - ``CORE_REG_STALL``
    - Writing 1 to bit '0' causes the CPU core to stall.

  * - 0x0201
    - ``CORE_REG_UPPER``
    - Bit 0 contains MSB (most significant bit) of the corresponding SPR address in the CPU core.

  * - 0x8000 - 0xFFFF
    - ``CDM_REG_ADDR``
    - Bits [14:0] of the corresponding SPR address in the CPU core. 


The address of the SPR (Special-Purpose Register) in the CPU core can be determined by the following operation:

.. code::

   SPR_REG_ADDR = CORE_REG_UPPER << 15 | CDM_REG_ADDR - 0x8000  

Core Stall Register (``CORE_REG_STALL``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: 0x0200
- Reset Value: 0
- Access: read-write

The register is used to stall the CPU core. Setting bit 0 as logic '1' causes the CPU core to stall.

Core Upper Register (``CORE_REG_UPPER``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: 0x0201
- Reset Value: 0
- Access: read-write

The register contains MSB of the SPR address as specified in the core. 

CDM Address Register (``CDM_REG_ADDR``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: 0x8000-0xFFFF
- Reset Value: *implementation specific*
- Access: *implementation specific*

The register's bits [14:0] contain the corresponding SPR address bits as specified in the core. 


