# Finslib API Reference

### FINS data types

|Name|Description|
|:---|:---|
|**`FINS_DATA_TYPE_BCD16`**|16 bit BCD between 0 and 9999|
|**`FINS_DATA_TYPE_BCD32`**|32 bit BCD between 0 and 99999999|
|**`FINS_DATA_TYPE_BIT`**|Single bit|
|**`FINS_DATA_TYPE_BIT_FORCED`**|Single bit with it's forced status|
|**`FINS_DATA_TYPE_DOUBLE`**|64 bit floating point in IEEE 754 format|
|**`FINS_DATA_TYPE_FLOAT`**|32 bit floating point in IEEE 754 format|
|**`FINS_DATA_TYPE_INT16`**|Signed 16 bit integer|
|**`FINS_DATA_TYPE_INT32`**|Signed 32 bit integer|
|**`FINS_DATA_TYPE_SBCD16_0`**|16 bit signed BCD type 0 between -999 and 999|
|**`FINS_DATA_TYPE_SBCD16_1`**|16 bit signed BCD type 1 between -7999 and 7999|
|**`FINS_DATA_TYPE_SBCD16_2`**|16 bit signed BCD type 2 between -999 and 9999|
|**`FINS_DATA_TYPE_SBCD16_3`**|16 bit signed BCD type 3 between -1999 and 9999|
|**`FINS_DATA_TYPE_SBCD32_0`**|32 bit signed BCD type 0 between -9999999 and 9999999|
|**`FINS_DATA_TYPE_SBCD32_1`**|32 bit signed BCD type 1 between -79999999 and 79999999|
|**`FINS_DATA_TYPE_SBCD32_2`**|32 bit signed BCD type 2 between -9999999 and 99999999|
|**`FINS_DATA_TYPE_SBCD32_3`**|32 bit signed BCD type 3 between -19999999 and 99999999|
|**`FINS_DATA_TYPE_UINT16`**|Unsigned 16 bit integer|
|**`FINS_DATA_TYPE_UINT32`**|Unsigned 32 bit integer|
|**`FINS_DATA_TYPE_WORD_FORCED`**|16 bit values with their forced status returned in four two 16 bit words|

### Description

The basic data types in a PLC are 16 bit words and bits but several functions also support other data types which are then mapped in one or more adjacent 16 bit words. The LibFINS data read and write functions support all the data types the PLC recognizes and translates them directly to and from equivalent computer data types making the exchange of data of several types between the PLC and a computer an easy task.

The constants `FINS_DATA_TYPE_...` are used in the call to [`finslib_multiple_memory_area_read()`](finslib_multiple_memory_area_read.md) and in calls which support signed binary BCD values to distinguish between the several different signed BCD implementations.

### See Also

* [`finslib_bcd_to_int();`](finslib_bcd_to_int.md)
* [`finslib_int_to_bcd();`](finslib_int_to_bcd.md)
* [`finslib_memory_area_read_sbcd16();`](finslib_memory_area_read_sbcd16.md)
* [`finslib_memory_area_read_sbcd32();`](finslib_memory_area_read_sbcd32.md)
* [`finslib_memory_area_write_sbcd16();`](finslib_memory_area_write_sbcd16.md)
* [`finslib_memory_area_write_sbcd32();`](finslib_memory_area_write_sbcd32.md)
* [`finslib_multiple_memory_area_read();`](finslib_multiple_memory_area_read.md)
