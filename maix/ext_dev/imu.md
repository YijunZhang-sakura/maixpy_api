---
title: maix.ext_dev.imu
---

maix.ext_dev.imu module


> You can use `maix.ext_dev.imu` to access this module with MaixPy
> This module is generated from [MaixPy](https://github.com/sipeed/MaixPy) and [MaixCDK](https://github.com/sipeed/MaixCDK)

## Module {#Module}

No module


## Enum {#Enum}

### Mode {#Mode}

imu mode

| item | describe |
| --- | --- |
| **values** | **ACC_ONLY**: <br>**GYRO_ONLY**: <br>**DUAL**: <br>
> C++ defination code:
> ```cpp
> enum class Mode {
>     ACC_ONLY = 0,
>     GYRO_ONLY,
>     DUAL
> }
> ```
### AccScale {#AccScale}

imu acc scale

| item | describe |
| --- | --- |
| **values** | **ACC_SCALE_2G**: <br>**ACC_SCALE_4G**: <br>**ACC_SCALE_8G**: <br>**ACC_SCALE_16G**: <br>
> C++ defination code:
> ```cpp
> enum class AccScale {
>     ACC_SCALE_2G = 0,
>     ACC_SCALE_4G,
>     ACC_SCALE_8G,
>     ACC_SCALE_16G
> }
> ```
### AccOdr {#AccOdr}

imu acc output data rate

| item | describe |
| --- | --- |
| **values** | **ACC_ODR_8000**: Accelerometer ODR set to 8000 Hz.<br>**ACC_ODR_4000**: Accelerometer ODR set to 4000 Hz.<br>**ACC_ODR_2000**: Accelerometer ODR set to 2000 Hz.<br>**ACC_ODR_1000**: Accelerometer ODR set to 1000 Hz.<br>**ACC_ODR_500**: Accelerometer ODR set to 500 Hz.<br>**ACC_ODR_250**: Accelerometer ODR set to 250 Hz.<br>**ACC_ODR_125**: Accelerometer ODR set to 125 Hz.<br>**ACC_ODR_62_5**: Accelerometer ODR set to 62.5 Hz.<br>**ACC_ODR_31_25**: Accelerometer ODR set to 31.25 Hz.<br>**ACC_ODR_128**: Accelerometer ODR set to 128 Hz.<br>**ACC_ODR_21**: Accelerometer ODR set to 21 Hz.<br>**ACC_ODR_11**: Accelerometer ODR set to 11 Hz.<br>**ACC_ODR_3**: Accelerometer ODR set to 3 Hz.<br>
> C++ defination code:
> ```cpp
> enum class AccOdr {
>     ACC_ODR_8000,      // Accelerometer ODR set to 8000 Hz.
>     ACC_ODR_4000,      // Accelerometer ODR set to 4000 Hz.
>     ACC_ODR_2000,      // Accelerometer ODR set to 2000 Hz.
>     ACC_ODR_1000,      // Accelerometer ODR set to 1000 Hz.
>     ACC_ODR_500,       // Accelerometer ODR set to 500 Hz.
>     ACC_ODR_250,       // Accelerometer ODR set to 250 Hz.
>     ACC_ODR_125,       // Accelerometer ODR set to 125 Hz.
>     ACC_ODR_62_5,      // Accelerometer ODR set to 62.5 Hz.
>     ACC_ODR_31_25,     // Accelerometer ODR set to 31.25 Hz.
>     ACC_ODR_128 = 12,  // Accelerometer ODR set to 128 Hz.
>     ACC_ODR_21,        // Accelerometer ODR set to 21 Hz.
>     ACC_ODR_11,        // Accelerometer ODR set to 11 Hz.
>     ACC_ODR_3,         // Accelerometer ODR set to 3 Hz.
> }
> ```
### GyroScale {#GyroScale}

imu gyro scale

| item | describe |
| --- | --- |
| **values** | **GYRO_SCALE_16DPS**: Gyroscope scale set to ±16 degrees per second.<br>**GYRO_SCALE_32DPS**: Gyroscope scale set to ±32 degrees per second.<br>**GYRO_SCALE_64DPS**: Gyroscope scale set to ±64 degrees per second.<br>**GYRO_SCALE_128DPS**: Gyroscope scale set to ±128 degrees per second.<br>**GYRO_SCALE_256DPS**: Gyroscope scale set to ±256 degrees per second.<br>**GYRO_SCALE_512DPS**: Gyroscope scale set to ±512 degrees per second.<br>**GYRO_SCALE_1024DPS**: Gyroscope scale set to ±1024 degrees per second.<br>**GYRO_SCALE_2048DPS**: Gyroscope scale set to ±2048 degrees per second.<br>
> C++ defination code:
> ```cpp
> enum class GyroScale {
>     GYRO_SCALE_16DPS = 0,       // Gyroscope scale set to ±16 degrees per second.
>     GYRO_SCALE_32DPS,            // Gyroscope scale set to ±32 degrees per second.
>     GYRO_SCALE_64DPS,            // Gyroscope scale set to ±64 degrees per second.
>     GYRO_SCALE_128DPS,           // Gyroscope scale set to ±128 degrees per second.
>     GYRO_SCALE_256DPS,           // Gyroscope scale set to ±256 degrees per second.
>     GYRO_SCALE_512DPS,           // Gyroscope scale set to ±512 degrees per second.
>     GYRO_SCALE_1024DPS,          // Gyroscope scale set to ±1024 degrees per second.
>     GYRO_SCALE_2048DPS,          // Gyroscope scale set to ±2048 degrees per second.
> }
> ```
### GyroOdr {#GyroOdr}

imu gyro output data rate

| item | describe |
| --- | --- |
| **values** | **GYRO_ODR_8000**: Gyroscope ODR set to 8000 Hz.<br>**GYRO_ODR_4000**: Gyroscope ODR set to 4000 Hz.<br>**GYRO_ODR_2000**: Gyroscope ODR set to 2000 Hz.<br>**GYRO_ODR_1000**: Gyroscope ODR set to 1000 Hz.<br>**GYRO_ODR_500**: Gyroscope ODR set to 500 Hz.<br>**GYRO_ODR_250**: Gyroscope ODR set to 250 Hz.<br>**GYRO_ODR_125**: Gyroscope ODR set to 125 Hz.<br>**GYRO_ODR_62_5**: Gyroscope ODR set to 62.5 Hz.<br>**GYRO_ODR_31_25**: Gyroscope ODR set to 31.25 Hz.<br>
> C++ defination code:
> ```cpp
> enum class GyroOdr {
>     GYRO_ODR_8000,     // Gyroscope ODR set to 8000 Hz.
>     GYRO_ODR_4000,     // Gyroscope ODR set to 4000 Hz.
>     GYRO_ODR_2000,     // Gyroscope ODR set to 2000 Hz.
>     GYRO_ODR_1000,     // Gyroscope ODR set to 1000 Hz.
>     GYRO_ODR_500,      // Gyroscope ODR set to 500 Hz.
>     GYRO_ODR_250,      // Gyroscope ODR set to 250 Hz.
>     GYRO_ODR_125,      // Gyroscope ODR set to 125 Hz.
>     GYRO_ODR_62_5,     // Gyroscope ODR set to 62.5 Hz.
>     GYRO_ODR_31_25,    // Gyroscope ODR set to 31.25 Hz.
> }
> ```


## Variable {#Variable}



## Function {#Function}



## Class {#Class}

### IMU {#IMU}

QMI8656 driver class


> C++ defination code:
> ```cpp
> class IMU
> ```

#### \_\_init\_\_ {#\_\_init\_\_}

```python
def __init__(self, driver: str, i2c_bus: int = -1, addr: int = 107, freq: int = 400000, mode: Mode = ..., acc_scale: AccScale = ..., acc_odr: AccOdr = ..., gyro_scale: GyroScale = ..., gyro_odr: GyroOdr = ..., block: bool = True) -> None
```
Construct a new IMU object, will open IMU

| item | description |
| --- | --- |
| **type** | func |
| **param** | **driver**: driver name, only support "qmi8656"<br>**i2c_bus**: i2c bus number. Automatically selects the on-board imu when -1 is passed in.<br>**addr**: IMU i2c addr.<br>**freq**: IMU freq<br>**mode**: IMU Mode: ACC_ONLY/GYRO_ONLY/DUAL<br>**acc_scale**: acc scale, see @imu::AccScale<br>**acc_odr**: acc output data rate, see @imu::AccOdr<br>**gyro_scale**: gyro scale, see @imu::GyroScale<br>**gyro_odr**: gyro output data rate, see @imu::GyroOdr<br>**block**: block or non-block, defalut is true<br>|
| **static** | False |

> C++ defination code:
> ```cpp
> IMU(std::string driver, int i2c_bus=-1, int addr=0x6B, int freq=400000,
>             maix::ext_dev::imu::Mode mode=maix::ext_dev::imu::Mode::DUAL,
>             maix::ext_dev::imu::AccScale acc_scale=maix::ext_dev::imu::AccScale::ACC_SCALE_2G,
>             maix::ext_dev::imu::AccOdr acc_odr=maix::ext_dev::imu::AccOdr::ACC_ODR_8000,
>             maix::ext_dev::imu::GyroScale gyro_scale=maix::ext_dev::imu::GyroScale::GYRO_SCALE_16DPS,
>             maix::ext_dev::imu::GyroOdr gyro_odr=maix::ext_dev::imu::GyroOdr::GYRO_ODR_8000,
>             bool block=true)
> ```
#### read {#read}

```python
def read(self) -> list[float]
```
Read data from IMU.

| item | description |
| --- | --- |
| **type** | func |
| **return** | list type. If only one of the outputs is initialized, only [x,y,z] of that output will be returned.<br>If all outputs are initialized, [acc_x, acc_y, acc_z, gyro_x, gyro_y, gyro_z] is returned. |
| **static** | False |

> C++ defination code:
> ```cpp
> std::vector<float> read()
> ```
#### calculate\_calibration {#calculate\_calibration}

```python
def calculate_calibration(self, time_ms: int = 30000) -> maix.err.Err
```
Caculate calibration, save calibration data to /maixapp/shart/imu_calibration

| item | description |
| --- | --- |
| **type** | func |
| **param** | **time_ms**: caculate max time, unit:ms<br>|
| **return** | err::Err |
| **static** | False |

> C++ defination code:
> ```cpp
> err::Err calculate_calibration(uint64_t time_ms = 30 * 1000)
> ```
#### get\_calibration {#get\_calibration}

```python
def get_calibration(self) -> list[float]
```
Get calibration data

| item | description |
| --- | --- |
| **type** | func |
| **return** | return an array, format is [acc_x_bias, acc_y_bias, acc_z_bias, gyro_x_bias, gyro_y_bias, gyro_z_bias]<br>If the calibration file cannot be found, an empty array will be returned. |
| **static** | False |

> C++ defination code:
> ```cpp
> std::vector<double> get_calibration()
> ```
### Gcsv {#Gcsv}

Gcsv class


> C++ defination code:
> ```cpp
> class Gcsv
> ```

#### \_\_init\_\_ {#\_\_init\_\_-2}

```python
def __init__(self) -> None
```
Construct a new IMU object

| item | description |
| --- | --- |
| **type** | func |
| **static** | False |

> C++ defination code:
> ```cpp
> Gcsv()
> ```
#### open {#open}

```python
def open(self, path: str, tscale: float = 0.001, gscale: float = 1, ascale: float = 1, mscale: float = 1, version: str = '1.3', id: str = 'imu', orientation: str = 'YxZ') -> maix.err.Err
```
Open a file

| item | description |
| --- | --- |
| **type** | func |
| **param** | **path**: the path where data will be saved<br>**tscale**: time scale, default is 0.001<br>**gscale**: gyroscope scale factor, default is 1, unit:g<br>**ascale**: accelerometer scale factor, default is 1, unit:radians/second<br>**mscale**: magnetometer scale factor, default is 1(unused)<br>**version**: version number, default is "1.3"<br>**id**: identifier for the IMU, default is "imu"<br>**orientation**: sensor orientation, default is "YxZ"<br>|
| **return** | error code |
| **static** | False |

> C++ defination code:
> ```cpp
> err::Err open(std::string path, double tscale = 0.001, double gscale = 1, double ascale = 1, double mscale = 1, std::string version = "1.3", std::string id = "imu", std::string orientation = "YxZ")
> ```
#### close {#close}

```python
def close(self) -> maix.err.Err
```
Close file

| item | description |
| --- | --- |
| **type** | func |
| **return** | error code |
| **static** | False |

> C++ defination code:
> ```cpp
> err::Err close()
> ```
#### is\_opened {#is\_opened}

```python
def is_opened(self) -> bool
```
Check if the object is already open

| item | description |
| --- | --- |
| **type** | func |
| **return** | true, opened; false, not opened |
| **static** | False |

> C++ defination code:
> ```cpp
> bool is_opened()
> ```
#### write {#write}

```python
def write(self, timestamp: float, gyro: list[float], acc: list[float], mag: list[float] = []) -> maix.err.Err
```
Write imu data to gcsv file

| item | description |
| --- | --- |
| **type** | func |
| **param** | **t**: Timestamp of the current data. The actual value is equal to t * tscale. unit:s<br>**gyro**: Gyroscope data must be an array consisting of x, y, and z-axis data. The actual value is equal to gyro * gscale. unit:g<br>**acc**: Acceleration data must be an array consisting of x, y, and z-axis data. The actual value is equal to acc * ascale.unit:radians/second<br>**mag**: Magnetic data must be an array consisting of x, y, and z-axis data. Currently not supported.<br>|
| **static** | False |

> C++ defination code:
> ```cpp
> err::Err write(double timestamp, std::vector<double> gyro, std::vector<double> acc, std::vector<double> mag = std::vector<double>())
> ```
