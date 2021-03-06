# SAS macros

Collection of SAS macros

## Reshape wide to long

There are multiple ways to transpose data. The `%multilong()` macro is inspired by the macro method mentioned [here](http://easysas.blogspot.com/2011/01/reshape-data-set-from-wide-to-long.html). It uses the `%wvlist()` macro supplied with the [RAND HRS Longitudinal File](https://www.rand.org/well-being/social-and-behavioral-policy/centers/aging/dataprod/hrs-data.html). The `%wvlist()` macro can be downloaded [here](https://hrs.isr.umich.edu/data-products/access-to-public-data).
To use the `%wvlist()` macro, the variable names in the data need to be in the format of RxSTEM. For example, the following data
  
| ID |  R1MSTAT |  R2MSTAT |  R3MSTAT |  R4MSTAT |  R1AGEY_B |  R2AGEY_B |  R3AGEY_B |  R4AGEY_B |
|----|----------|----------|----------|----------|-----------|-----------|-----------|-----------|
| 1  |          |          |          |          |           |           |           |           |
| 2  |          |          |          |          |           |           |           |           |

will be transposed into

| ID |  WAVE |  RxMSTAT |  RxAGEY_B |
|----|-------|----------|-----------|
| 1  | 1     |          |           |
| 1  | 2     |          |           |
| 1  | 3     |          |           |
| 1  | 4     |          |           |
| 2  | 1     |          |           |
| 2  | 2     |          |           |
| 2  | 3     |          |           |
| 2  | 4     |          |           |

## Calculate age
Sara Adams and Chris Colby wrote an [article](https://www.lexjansen.com/wuss/2009/cod/COD-Adams.pdf) on how to accurately calculate interger and continuous age. The macro can be found in the appendix.  
