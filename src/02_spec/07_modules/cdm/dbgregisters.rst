Programmer Interface: Control Registers
---------------------------------------

The Control Debug Module implements the :ref:`sec:spec:api:base_register_map`.
The reset values are to be decided.

.. tabularcolumns:: |p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.40\linewidth-2\tabcolsep}|p{\dimexpr 0.20\linewidth-2\tabcolsep}|
.. flat-table:: CDM-OR1K base register reset values
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

Additionally, it implements the following debug control registers of or1k CPU core for CDM-specific functionality.


.. tabularcolumns:: |p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.60\linewidth-2\tabcolsep}|
.. flat-table:: CDM-OR1K register map
  :widths: 2 2 6
  :header-rows: 1

  * - address
    - name
    - description

  * - 0x0200
    - ``DEBUG_VALUE_REG0_0``
    - Bits [15:0] (least significant bits) DVR0

  * - 0x0201
    - ``DEBUG_VALUE_REG0_1``
    - Bits [31:16] of DVR0
   
  * - 0x0202
    - ``DEBUG_VALUE_REG1_0``
    - Bits [15:0] (least significant bits) of DVR1

  * - 0x0280
    - ``DEBUG_VALUE_REG1_1``
    - Bits [31:16] of DVR1

  * - 0x0281
    - ``DEBUG_VALUE_REG2_0``
    - Bits [15:0] (least significant bits) of DVR2

  * - 0x0282
    - ``DEBUG_VALUE_REG2_1``
    - Bits [31:16] of DVR2

  * - 0x0283
    - ``DEBUG_VALUE_REG3_0``
    - Bits [15:0] (least significant bits) of DVR3

  * - 0x0284
    - ``DEBUG_VALUE_REG3_1``
    - Bits [31:16] of DVR3

  * - 0x0285
    - ``DEBUG_VALUE_REG4_0``
    - Bits [15:0] (least significant bits) of DVR4

  * - 0x0286
    - ``DEBUG_VALUE_REG4_1``
    - Bits [31:16] of DVR4

  * - 0x0287
    - ``DEBUG_VALUE_REG5_0``
    - Bits [15:0] (least significant bits) of DVR5

  * - 0x0290
    - ``DEBUG_VALUE_REG5_1``
    - Bits [31:16] of DVR5

  * - 0x0291
    - ``DEBUG_VALUE_REG6_0``
    - Bits [15:0] (least significant bits) of DVR6

  * - 0x0292
    - ``DEBUG_VALUE_REG6_1``
    - Bits [31:16] of DVR6

  * - 0x0293
    - ``DEBUG_VALUE_REG7_0``
    - Bits [15:0] (least significant bits) of DVR7

  * - 0x0294
    - ``DEBUG_VALUE_REG7_1``
    - Bits [31:16] of DVR7

  * - 0x0295
    - ``DEBUG_CTRL_REG0_0``
    - Bits [15:0] (least significant bits) of DCR0

  * - 0x0296
    - ``DEBUG_CTRL_REG0_1``
    - Bits [31:16] of DCR0

  * - 0x0297
    - ``DEBUG_CTRL_REG1_0``
    - Bits [15:0] (least significant bits) of DCR1

  * - 0x02A0
    - ``DEBUG_CTRL_REG1_1``
    - Bits [31:16] of DCR1

  * - 0x02A1
    - ``DEBUG_CTRL_REG2_0``
    - Bits [15:0] (least significant bits) of DCR2

  * - 0x02A2
    - ``DEBUG_CTRL_REG2_1``
    - Bits [31:16] of DCR2

  * - 0x02A3
    - ``DEBUG_CTRL_REG3_0``
    - Bits [15:0] (least significant bits) of DCR3

  * - 0x02A4
    - ``DEBUG_CTRL_REG3_1``
    - Bits [31:16] of DCR3

  * - 0x02A5
    - ``DEBUG_CTRL_REG4_0``
    - Bits [15:0] (least significant bits) of DCR4

  * - 0x02A6
    - ``DEBUG_CTRL_REG4_1``
    - Bits [31:16] of DCR4

  * - 0x02A7
    - ``DEBUG_CTRL_REG5_0``
    - Bits [15:0] (least significant bits) of DCR5

  * - 0x02B0
    - ``DEBUG_CTRL_REG5_1``
    - Bits [31:16] of DCR5

  * - 0x02B1
    - ``DEBUG_CTRL_REG6_0``
    - Bits [15:0] (least significant bits) of DCR6

  * - 0x02B2
    - ``DEBUG_CTRL_REG6_1``
    - Bits [31:16] of DCR6

  * - 0x02B3
    - ``DEBUG_CTRL_REG7_0``
    - Bits [15:0] (least significant bits) of DCR7

  * - 0x02B4
    - ``DEBUG_CTRL_REG7_1``
    - Bits [31:16] of DCR7

  * - 0x02B5
    - ``DEBUG_MODE_REG1_0``
    - Bits [15:0] (least significant bits) of DMR1

  * - 0x02B6
    - ``DEBUG_MODE_REG1_1``
    - Bits [31:16] of DMR1

  * - 0x02B7
    - ``DEBUG_MODE_REG2_0``
    - Bits [15:0] (least significant bits) of DMR2

  * - 0x02C0
    - ``DEBUG_MODE_REG2_1``
    - Bits [31:16] of DMR2

  * - 0x02C1
    - ``DEBUG_WC_REG0_0``
    - Bits [15:0] (least significant bits) of Debug Watchpoint Counter 0

  * - 0x02C2
    - ``DEBUG_WC_REG0_1``
    - Bits [31:16] of Debug Watchpoint Counter 0

  * - 0x02C3
    - ``DEBUG_WC_REG1_0``
    - Bits [15:0] (least significant bits) of Debug Watchpoint Counter 1

  * - 0x02C4
    - ``DEBUG_WC_REG1_1``
    - Bits [31:16] of Debug Watchpoint Counter 1

  * - 0x02C5
    - ``DEBUG_STOP_REG_0``
    - Bits [15:0] (least significant bits) of Debug Stop Register

  * - 0x02C6
    - ``DEBUG_STOP_REG_1``
    - Bits [31:16] of Debug Stop Register

  * - 0x02C7
    - ``DEBUG_REASON_REG_0``
    - Bits [15:0] (least significant bits) of Debug Reason Register

  * - 0x02D0
    - ``DEBUG_REASON_REG_1``
    - Bits [31:16] of Debug Reason Register

  * - 0x02D1
    - ``DEBUG_CFG_REG_0``
    - Bits [15:0] (least significant bits) of Debug Configuration Register

  * - 0x02D2
    - ``DEBUG_CFG_REG_1``
    - Bits [31:16] of Debug Configuration Register

  * - 0x02D3
    - ``DEBUG_WRITE_UPDATE``
    - Bit 0 of this register will be used to commit write data
 


Debug Value Registers (``DEBUG_VALUE_REG*_*``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: *see full register map above*
- Reset Value: 0
- Access: read-write

The debug value registers (DVRs) are 32-bit special-purpose supervisor-level registers programmed with the watchpoint/breakpoint addresses or data.

Debug Control Registers (``DEBUG_CTRL_REG*_*``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: *see full register map above*
- Reset Value: 0
- Access: *see below*

The debug control registers (DCRs) are 32-bit special-purpose supervisor-level registers.
The DCRs are programmed with the watchpoint settings that define how DVRs are compared to the instruction fetch or load/store address or to the load/store data.

.. tabularcolumns:: |p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.40\linewidth-2\tabcolsep}|p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.20\linewidth-2\tabcolsep}|
.. flat-table:: DCR Field Description
  :widths: 2 4 2 2   
  :header-rows: 1

  * - bits
    - identifier
    - reset
    - Access

  * - 31-8
    - Reserved
    - X
    - R

  * - 7-5
    - Compare To Condition
    - 0
    - R/W

  * - 4
    - Signed Comparison
    - 0
    - R/W

  * - 3-1
    - Compare Condition
    - 0
    - R/W

  * - 0
    - DVR/DCR Present
    - 0
    - R	
  

Debug Mode Register1 (``DEBUG_MODE_REG1_*``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: *see full register map above*
- Reset Value: X (bits: 31-25) | 0 (bits: 23-0)
- Access: read (bits: 31-25) | read-write (bits: 23-0)

The debug mode register 1 is a 32-bit special-purpose supervisor-level register programmed with the watchpoint/breakpoint settings that define
how DVR/DCR pairs operate.

Debug Mode Register2 (``DEBUG_MODE_REG2_*``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: *see full register map above*
- Reset Value: 0
- Access: read (bits: 31-22) | read-write (bits: 21-0)

The debug mode register 1 is a 32-bit special-purpose supervisor-level register.
The DMR2 is programmed with the watchpoint/breakpoint settings that define which watchpoints generate a breakpoint and which watchpoint counters are enabled.


Debug Watchpoint Counter Registers (``DEBUG_WC_REG*_*``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: *see full register map above*
- Reset Value: 0
- Access: read-write

The debug watchpoint counter registers are 32-bit special-purpose supervisor-level registers.
The DWCRs contain 16-bit counters that count watchpoints programmed in the DMR and 16-bit match values. When a counter reaches the match value, a watchpoint is generated.


Debug Stop Register (``DEBUG_STOP_REG_*``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: *see full register map above*
- Reset Value: X (bits: 31-14) | 0 (bits: 13-0)
- Access: read (bits: 31-14) | read-write (bits: 13-0)

The debug stop counter registers are 32-bit special-purpose supervisor-level registers.
The DSR specifies which exceptions cause the core to stop the execution of the exception handler and turn over control to development interface.


Debug Reason Register (``DEBUG_REASON_REG_*``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: *see full register map above*
- Reset Value: X (bits: 31-14) | 0 (bits: 13-0)
- Access: read (bits: 31-14) | read-write (bits: 13-0)

The debug reason counter registers are 32-bit special-purpose supervisor-level registers.
The DRR specifies which event caused the core to stop the execution of program flow and turned control over to the development interface.


Debug Configuration Register (``DEBUG_CFG_REG_*``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: *see full register map above*
- Reset Value: -
- Access: read 

The debug configuration counter registers are 32-bit special-purpose supervisor-level registers.
It specifies debug unit capabilities and configuration.


Debug Update Write Register (``DEBUG_WRITE_UPDATE``)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Address: 0x02D3
- Reset Value: 0
- Access: read-write 

The debug update write register's bit 0 is used a signal to commit write date correctly.


