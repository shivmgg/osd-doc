Programmer Interface: Control Registers
---------------------------------------

The Control Debug Module implements the :ref:`sec:spec:api:base_register_map`.
The reset values are to be decided.

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
    - ?

  * - 0x0001
    - ``MOD_TYPE``
    - module type identifier
    - ?

  * - 0x0002
    - ``MOD_VERSION``
    - module version
    - ?

  * - 0x0003
    - ``MOD_CS``
    - module control and status
    - ?

  * - 0x0004
    - ``MOD_EVENT_DEST``
    - destination of debug events
    - ?

Additionally, it implements the following debug control registers of or1k CPU core for CDM-specific functionality.


.. tabularcolumns:: |p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.20\linewidth-2\tabcolsep}|p{\dimexpr 0.60\linewidth-2\tabcolsep}|
.. flat-table:: CDM register map
  :widths: 2 2 6
  :header-rows: 1

  * - address
    - name
    - description

  * - 0x0200
    - ``DEBUG_VALUE_REG_0_0``
    - Bits [15:0] (least significant bits) DVR0

  * - 0x0201
    - ``DEBUG_VALUE_REG_0_1``
    - Bits [31:16] of DVR0
   
  * - 0x0202
    - ``DEBUG_VALUE_REG_1_0``
    - Bits [15:0] (least significant bits) of DVR1

  * - 0x0280
    - ``DEBUG_VALUE_REG_1_1``
    - Bits [31:16] of DVR1

  * - 0x0281
    - ``DEBUG_VALUE_REG_2_0``
    - Bits [15:0] (least significant bits) of DVR2

  * - 0x0282
    - ``DEBUG_VALUE_REG_2_1``
    - Bits [31:16] of DVR2

  * - 0x0283
    - ``DEBUG_VALUE_REG_3_0``
    - Bits [15:0] (least significant bits) of DVR3

  * - 0x0284
    - ``DEBUG_VALUE_REG_3_1``
    - Bits [31:16] of DVR3

  * - 0x0285
    - ``DEBUG_VALUE_REG_4_0``
    - Bits [15:0] (least significant bits) of DVR4

  * - 0x0286
    - ``DEBUG_VALUE_REG_4_1``
    - Bits [31:16] of DVR4

  * - 0x0287
    - ``DEBUG_VALUE_REG_5_0``
    - Bits [15:0] (least significant bits) of DVR5

  * - 0x0290
    - ``DEBUG_VALUE_REG_5_1``
    - Bits [31:16] of DVR5

  * - 0x0291
    - ``DEBUG_VALUE_REG_6_0``
    - Bits [15:0] (least significant bits) of DVR6

  * - 0x0292
    - ``DEBUG_VALUE_REG_6_1``
    - Bits [31:16] of DVR6

  * - 0x0293
    - ``DEBUG_VALUE_REG_7_0``
    - Bits [15:0] (least significant bits) of DVR7

  * - 0x0294
    - ``DEBUG_VALUE_REG_7_1``
    - Bits [31:16] of DVR7

  * - 0x0295
    - ``DEBUG_CTRL_REG_0_0``
    - Bits [15:0] (least significant bits) of DCR0

  * - 0x0296
    - ``DEBUG_CTRL_REG_0_1``
    - Bits [31:16] of DCR0

  * - 0x0297
    - ``DEBUG_CTRL_REG_1_0``
    - Bits [15:0] (least significant bits) of DCR1

  * - 0x02A0
    - ``DEBUG_CTRL_REG_1_1``
    - Bits [31:16] of DCR1

  * - 0x02A1
    - ``DEBUG_CTRL_REG_2_0``
    - Bits [15:0] (least significant bits) of DCR2

  * - 0x02A2
    - ``DEBUG_CTRL_REG_2_1``
    - Bits [31:16] of DCR2

  * - 0x02A3
    - ``DEBUG_CTRL_REG_3_0``
    - Bits [15:0] (least significant bits) of DCR3

  * - 0x02A4
    - ``DEBUG_CTRL_REG_3_1``
    - Bits [31:16] of DCR3

  * - 0x02A5
    - ``DEBUG_CTRL_REG_4_0``
    - Bits [15:0] (least significant bits) of DCR4

  * - 0x02A6
    - ``DEBUG_CTRL_REG_4_1``
    - Bits [31:16] of DCR4

  * - 0x02A7
    - ``DEBUG_CTRL_REG_5_0``
    - Bits [15:0] (least significant bits) of DCR5

  * - 0x02B0
    - ``DEBUG_CTRL_REG_5_1``
    - Bits [31:16] of DCR5

  * - 0x02B1
    - ``DEBUG_CTRL_REG_6_0``
    - Bits [15:0] (least significant bits) of DCR6

  * - 0x02B2
    - ``DEBUG_CTRL_REG_6_1``
    - Bits [31:16] of DCR6

  * - 0x02B3
    - ``DEBUG_CTRL_REG_7_0``
    - Bits [15:0] (least significant bits) of DCR7

  * - 0x02B4
    - ``DEBUG_CTRL_REG_7_1``
    - Bits [31:16] of DCR7

  * - 0x02B5
    - ``DEBUG_MODE_REG_1_0``
    - Bits [15:0] (least significant bits) of DMR1

  * - 0x02B6
    - ``DEBUG_MODE_REG_1_1``
    - Bits [31:16] of DMR1

  * - 0x02B7
    - ``DEBUG_MODE_REG_2_0``
    - Bits [15:0] (least significant bits) of DMR2

  * - 0x02C0
    - ``DEBUG_MODE_REG_2_1``
    - Bits [31:16] of DMR2

  * - 0x02C1
    - ``DEBUG_WC_REG_0_0``
    - Bits [15:0] (least significant bits) of Debug Watchpoint Counter 0

  * - 0x02C2
    - ``DEBUG_WC_REG_0_1``
    - Bits [31:16] of Debug Watchpoint Counter 0

  * - 0x02C3
    - ``DEBUG_WC_REG_1_0``
    - Bits [15:0] (least significant bits) of Debug Watchpoint Counter 1

  * - 0x02C4
    - ``DEBUG_WC_REG_1_1``
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

