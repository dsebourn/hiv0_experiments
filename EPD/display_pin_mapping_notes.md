// WISBLOCK IO 40 PIN CONNECTOR MAPPING
  /*
    Pin Number  Pin Name  Description
    1           VBAT	    Power supply from battery
    2	          VBAT	    Power supply from battery
    3		        GND	      Ground
    4		        GND	      Ground
    5	          3V3	      3.3V power supply
    6	          3V3_S	    3.3V power supply, controlled by CPU module
    7	          USB+	    USB D+
    8	          USB-	    USB D-
    9		        VBUS	    5V input for USB
    10	        SW1	      Switch connection
    11	        TX0	      MCU UART0 TX signal
    12	        RXD0	    MCU UART0 RX signal
    13	        RESET	    Reset switch, for MCU reset
    14	        LED1	    LED for battery charge indicator
    15	        LED2	    LED for custom used
    16	        LED3	    LED for custom used
    17	        VDD	      GPIO voltage and MCU module
    18	        VDD	      GPIO voltage and MCU module
    19	        I2C1_SDA	#1 I2C data signal
    20	        I2C1_SCL	#2 I2C clock signal
    21	        AIN0	    Analog input for ADC
    22	        AIN1	    Analog input for ADC
    23	        NC	      Not connected
    24	        NC	      Not connected
    25	        SPI_CS	  SPI chip select signal
    26	        SPI_CLK	  SPI clock
    27	        SPI_MISO	SPI MISO signal
    28	        SPI_MOSI	SPI MOSI signal
    29	        IO1	      General purpose IO
    30	        IO2	      Used for 3V3_S enable
    31	        IO3	      General purpose IO
    32	        IO4	      General purpose IO
    33	        TXD1	    MCU UART1 TX signal
    34	        RXD1	    MCU UART1 RX signal
    35	        I2C2_SDA	#2 I2C data signal
    36	        I2C2_SCL	#2 I2C clock signal
    37	        IO5	      General purpose IO
    38	        IO6	      General purpose IO
    39          GND       Ground
    40          GND       Ground
  */

// WISBLOCK RAK14000 DATASHEET MAPPING
  /*
    Pin Number  Pin Name  Description
    1           NC
    2	          NC	      Power supply from battery
    3		        GND	      Ground
    4		        GND	      Ground
    5	          NC
    6	          3V3_S	    3.3V power supply, controlled by CPU module
    7	          NC
    8	          NC
    9		        NC
    10	        NC
    11	        NC
    12	        NC
    13	        RESET	    Reset switch, for MCU reset
    14	        NC
    15	        NC
    16	        NC
    17	        NC
    18	        NC
    19	        NC
    20	        NC
    21	        NC
    22	        NC
    23	        NC
    24	        NC
    25	        SPI_CS	  SPI chip select signal
    26	        SPI_CLK	  SPI clock
    27	        NC
    28	        SPI_MOSI	SPI MOSI signal
    29	        NC
    30	        NC
    31	        IO3	      General purpose IO
    32	        IO4	      General purpose IO
    33	        NC
    34	        NC
    35	        NC
    36	        NC
    37	        IO5	      General purpose IO
    38	        IO6	      General purpose IO
    39          GND       Ground
    40          GND       Ground
  */

// SOLOMON SYSTECH SSD1680 CONTROLLER DATASHEET MAPPING
  /*
    //  UNABLE TO LOCATE EXACT PIN MAPPINGS, CMD TABLE ON PG 20 SOMEWHAT HELPS,
    //  NOT SURE HOW TO RE-MAP IN DRIVER BASED ON THESE COMMANDS:
    //  https://www.crystalfontz.com/controllers/uploaded/SSD1680.pdf
    //  COMMAND TABLE, PAGE 20:
    //  - 0x01  Driver Output Control
    //  - 0x03  Gate Driving voltage Control
    //  - 0x04  Source Driving voltage Control
    //  - 0x08  Initial Code Setting OTP Program
    //  - 0x09  Write Register for Initial Code Setting
    //  - 0x0A  Read Register for Initial Code Setting
    //  - 0x0C  Booster Soft start
    //  - 0x10  Deep Sleep mode
    //  - 0x11  Data Entry mode setting
    //  - 0x12  SW RESET 
    //  - 0x14  HV Ready Detection
    //  - 0x15  VCI Detection 
    //  - 0x20  Master Activation 
    //  - 0x21  Display Update Control 1
    //  - 0x22  Display Update Control 2
    //  - 0x24  Write RAM (Black White) / RAM 0x24
    //  - 0x27  Read RAM
    //  - 0x28  VCOM Sense
    //  - 0x29  VCOM Sense Duration
    //  - 0x2A  Program VCOM OTP
    //  - 0x2B  Write Register for VCOM Control
    //  - 0x2C  Write VCOM register
    //  - 0x2D  OTP Register Read for Display Option
    //  - 0x2E  User ID Read 
    //  - 0x2F  Status Bit Read
    //  - 0x30  Program WS OTP
    //  - 0x31  Load WS OTP
    //  - 0x32  Write LUT register 
    //  - 0x34  CRC calculation 
    //  - 0x35  CRC Status Read
    //  - 0x36  Program OTP selection 
    //  - 0x37  Write Register for Display Option
    //  - 0x38  Write Register for User ID
    //  - 0x39  OTP program mode
    //  - 0x3C  Border Waveform Control
    //  - 0x3F  End Option (EOPT) 
    //  - 0x41  Read RAM Option 
    //  - 0x44  Set RAM X - address Start / End position 
    //  - 0x45  Set Ram Y- address Start / End position 
    //  - 0x47  Auto Write B/W RAM for Regular Pattern 
    //  - 0x4E  Set RAM X address counter
    //  - 0x4F  Set RAM Y address counter
    //  - 0x7F  NOP
  */

// DRIVER CONFIGURATION - ADAFRUIT SSD1680 (B&W)
  /*
    #define SSD1680_DRIVER_CONTROL  0x01
    #define SSD1680_GATE_VOLTAGE    0x03
    #define SSD1680_SOURCE_VOLTAGE  0x04
    #define SSD1680_PROGOTP_INITIAL 0x08
    #define SSD1680_PROGREG_INITIAL 0x09
    #define SSD1680_READREG_INITIAL 0x0A
    #define SSD1680_BOOST_SOFTSTART 0x0C
    #define SSD1680_DEEP_SLEEP      0x10
    #define SSD1680_DATA_MODE       0x11
    #define SSD1680_SW_RESET        0x12
    #define SSD1680_TEMP_CONTROL    0x18
    #define SSD1680_TEMP_WRITE      0x1A
    #define SSD1680_MASTER_ACTIVATE 0x20
    #define SSD1680_DISP_CTRL1      0x21
    #define SSD1680_DISP_CTRL2      0x22
    #define SSD1680_WRITE_RAM1      0x24
    #define SSD1680_WRITE_RAM2      0x26
    #define SSD1680_WRITE_VCOM      0x2C
    #define SSD1680_READ_OTP        0x2D
    #define SSD1680_READ_STATUS     0x2F
    #define SSD1680_WRITE_LUT       0x32
    #define SSD1680_WRITE_BORDER    0x3C
    #define SSD1680_END_OPTION      0x3F
    #define SSD1680_SET_RAMXPOS     0x44
    #define SSD1680_SET_RAMYPOS     0x45
    #define SSD1680_SET_RAMXCOUNT   0x4E
    #define SSD1680_SET_RAMYCOUNT   0x4F
  */
  
// DISPLAY APPLICATION FILE RAK14000 EPAPER MONOCHROME
  /*
    #define POWER_ENABLE   WB_IO2 // ASSIGNED TO UNUSED PIN ON BOARD, MOVE TO PIN 6 3v3_S
    #define EPD_MOSI       MOSI  
    #define EPD_MISO       -1     // not use
    #define EPD_SCK        SCK   
    #define EPD_CS         SS    
    #define EPD_DC         WB_IO1
    #define SRAM_CS        -1     // not use
    #define EPD_RESET      -1     // not use
    #define EPD_BUSY       WB_IO4

    #define LEFT_BUTTON    WB_IO3
    #define MIDDLE_BUTTON  WB_IO5
    #define RIGHT_BUTTON   WB_IO6
  */

// FULL MAPPING TRANSLATIONS IN APPLICATION CODE
  /*
    #define POWER_ENABLE   WB_IO2   PIN 30
    #define EPD_MOSI       MOSI     PIN     // May get set to -1 (NA) due to Adafruit_SPIDevice mapping
    #define EPD_MISO       -1       
    #define EPD_SCK        SCK      PIN ??  // May get set to -1 (NA) due to Adafruit_SPIDevice mapping
    #define EPD_CS         SS       PIN ??  
    #define EPD_DC         WB_IO1   PIN 29
    #define SRAM_CS        -1     
    #define EPD_RESET      -1     
    #define EPD_BUSY       WB_IO4   PIN 32

    #define LEFT_BUTTON    WB_IO3   PIN 31
    #define MIDDLE_BUTTON  WB_IO5   PIN 37
    #define RIGHT_BUTTON   WB_IO6   PIN 38
  */

  /*
  Adafruit_SPIDevice::Adafruit_SPIDevice(int8_t cspin, uint32_t freq,
                                       BusIOBitOrder dataOrder,
                                       uint8_t dataMode, SPIClass *theSPI) {
  #ifdef BUSIO_HAS_HW_SPI
    _cs = cspin;
    _sck = _mosi = _miso = -1;
    _spi = theSPI;
    _begun = false;
    _spiSetting = new SPISettings(freq, dataOrder, dataMode);
    _freq = freq;
    _dataOrder = dataOrder;
    _dataMode = dataMode;
  #else
    // unused, but needed to suppress compiler warns
    (void)cspin;
    (void)freq;
    (void)dataOrder;
    (void)dataMode;
    (void)theSPI;
  #endif
  }
  */