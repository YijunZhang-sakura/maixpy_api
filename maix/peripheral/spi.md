---
title: maix.peripheral.spi
---

maix.peripheral.spi module


> You can use `maix.peripheral.spi` to access this module with MaixPy
> This module is generated from [MaixPy](https://github.com/sipeed/MaixPy) and [MaixCDK](https://github.com/sipeed/MaixCDK)

## Module {#Module}

No module


## Enum {#Enum}

### Mode {#Mode}

SPI mode enum

| item | describe |
| --- | --- |
| **values** | **MASTER**: spi master mode<br>**SLAVE**: spi slave mode<br>
> C++ defination code:
> ```cpp
> enum Mode
>     {
>         MASTER = 0x0, // spi master mode
>         SLAVE = 0x1,  // spi slave mode
>     }
> ```


## Variable {#Variable}



## Function {#Function}



## Class {#Class}

### SPI {#SPI}

Peripheral spi class


> C++ defination code:
> ```cpp
> class SPI
> ```

#### \_\_init\_\_ {#\_\_init\_\_}

```python
def __init__(self, id: int, mode: Mode, freq: int, polarity: int = 0, phase: int = 0, bits: int = 8, cs_enable: int = 0, soft_cs: bool = False, cs: str = 'GPIOA19') -> None
```
SPI constructor

| item | description |
| --- | --- |
| **type** | func |
| **param** | **id**: direction [in], spi bus id, int type<br>**mode**: direction [in], mode of spi, spi.Mode type, spi.Mode.MASTER or spi.Mode.SLAVE.<br>**freq**: direction [in], freq of spi, int type<br>**polarity**: direction [in], polarity of spi, 0 means idle level of clock is low, 1 means high, int type, default is 0.<br>**phase**: direction [in], phase of spi, 0 means data is captured on the first edge of the SPI clock cycle, 1 means second, int type, default is 0.<br>**bits**: direction [in], bits of spi, int type, default is 8.<br>**cs_enable**: direction [in], cs pin active level, default is 0(low)<br>**soft_cs**: direction [in], not use hardware cs, bool type, if set true, you can operate cs pin use gpio manually.<br>**cs**: direction [in], soft cs pin number, std::string type, default is "GPIOA19", if SPI support multi hardware cs, you can set it to other value.<br>|
| **static** | False |

> C++ defination code:
> ```cpp
> SPI(int id, spi::Mode mode, int freq, int polarity = 0, int phase = 0,
>             int bits = 8, unsigned char cs_enable=0, bool soft_cs = false, std::string cs = "GPIOA19")
> ```
#### read {#read}

```python
def read(*args, **kwargs)
```
read data from spi

| item | description |
| --- | --- |
| **type** | func |
| **param** | **length**: direction [in], read length, int type<br>|
| **return** | bytes data, Bytes type in C++, bytes type in MaixPy. You need to delete it manually after use in C++. |
| **static** | False |

> C++ defination code:
> ```cpp
> Bytes *read(int length)
> ```
#### write {#write}

```python
def write(self, data: maix.Bytes(bytes)) -> int
```
write data to spi

| item | description |
| --- | --- |
| **type** | func |
| **param** | **data**: direction [in], data to write, Bytes type in C++, bytes type in MaixPy<br>|
| **return** | write length, int type, if write failed, return -err::Err code. |
| **static** | False |

> C++ defination code:
> ```cpp
> int write(Bytes *data)
> ```
#### write\_read {#write\_read}

```python
def write_read(*args, **kwargs)
```
write data to spi and read data from spi at the same time.

| item | description |
| --- | --- |
| **type** | func |
| **param** | **data**: direction [in], data to write, Bytes type in C++, bytes type in MaixPy<br>**read_len**: direction [in], read length, int type, should > 0.<br>|
| **return** | read data, Bytes type in C++, bytes type in MaixPy. You need to delete it manually after use in C++. |
| **static** | False |

> C++ defination code:
> ```cpp
> Bytes *write_read(Bytes *data, int read_len)
> ```
#### is\_busy {#is\_busy}

```python
def is_busy(self) -> bool
```
get busy status of spi

| item | description |
| --- | --- |
| **type** | func |
| **return** | busy status, bool type |
| **static** | False |

> C++ defination code:
> ```cpp
> bool is_busy()
> ```
