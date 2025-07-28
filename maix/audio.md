---
title: maix.audio
---

maix.audio module


> You can use `maix.audio` to access this module with MaixPy
> This module is generated from [MaixPy](https://github.com/sipeed/MaixPy) and [MaixCDK](https://github.com/sipeed/MaixCDK)

## Module {#Module}

No module


## Enum {#Enum}

### Format {#Format}

Audio type

| item | describe |
| --- | --- |
| **values** | **FMT_NONE**: format invalid<br>**FMT_S8**: unsigned 8 bits<br>**FMT_S16_LE**: signed 16 bits, little endian<br>**FMT_S32_LE**: signed 32 bits, little endian<br>**FMT_S16_BE**: signed 16 bits, big endian<br>**FMT_S32_BE**: signed 32 bits, big endian<br>**FMT_U8**: unsigned 8 bits<br>**FMT_U16_LE**: unsigned 16 bits, little endian<br>**FMT_U32_LE**: unsigned 32 bits, little endian<br>**FMT_U16_BE**: unsigned 16 bits, big endian<br>**FMT_U32_BE**: unsigned 32 bits, big endian<br>
> C++ defination code:
> ```cpp
> enum Format
>     {
>         FMT_NONE = 0,       // format invalid
>         FMT_S8,             // unsigned 8 bits
>         FMT_S16_LE,         // signed 16 bits, little endian
>         FMT_S32_LE,         // signed 32 bits, little endian
>         FMT_S16_BE,         // signed 16 bits, big endian
>         FMT_S32_BE,         // signed 32 bits, big endian
>         FMT_U8,             // unsigned 8 bits
>         FMT_U16_LE,         // unsigned 16 bits, little endian
>         FMT_U32_LE,         // unsigned 32 bits, little endian
>         FMT_U16_BE,         // unsigned 16 bits, big endian
>         FMT_U32_BE,         // unsigned 32 bits, big endian
>     }
> ```


## Variable {#Variable}



## Function {#Function}



## Class {#Class}

### Recorder {#Recorder}

Recorder class


> C++ defination code:
> ```cpp
> class Recorder
> ```

#### \_\_init\_\_ {#\_\_init\_\_}

```python
def __init__(self, path: str = '', sample_rate: int = 48000, format: Format = ..., channel: int = 1, block: bool = True) -> None
```
Construct a new Recorder object. currectly only pcm and wav formats supported.

| item | description |
| --- | --- |
| **type** | func |
| **param** | **path**: record path. the path determines the location where you save the file, if path is none, the audio module will not save file.<br>**sample_rate**: record sample rate, default is 48000(48KHz), means 48000 samples per second.<br>**format**: record sample format, default is audio::Format::FMT_S16_LE, means sampling 16 bits at a time and save as signed 16 bits, little endian. see @audio::Format<br>**channel**: record sample channel, default is 1, means 1 channel sampling at the same time<br>**block**: block record, default is true, means block record, if false, record will not block<br>|
| **static** | False |

> C++ defination code:
> ```cpp
> Recorder(std::string path = std::string(), int sample_rate = 48000, audio::Format format = audio::Format::FMT_S16_LE, int channel = 1, bool block = true)
> ```
#### volume {#volume}

```python
def volume(self, value: int = -1) -> int
```
Set/Get record volume

| item | description |
| --- | --- |
| **type** | func |
| **param** | **value**: volume value, If you use this parameter, audio will set the value to volume,<br>if you don't, it will return the current volume. range is [0, 100].<br>|
| **return** | the current volume |
| **static** | False |

> C++ defination code:
> ```cpp
> int volume(int value = -1)
> ```
#### mute {#mute}

```python
def mute(self, data: int = -1) -> bool
```
Mute

| item | description |
| --- | --- |
| **type** | func |
| **param** | **data**: mute data, If you set this parameter to true, audio will set the value to mute,<br>if you don't, it will return the current mute status.<br>|
| **return** | Returns whether mute is currently enabled. |
| **static** | False |

> C++ defination code:
> ```cpp
> bool mute(int data = -1)
> ```
#### reset {#reset}

```python
def reset(self, start: bool = True) -> None
```
Reset record status

| item | description |
| --- | --- |
| **type** | func |
| **param** | **start**: start prepare audio data, default is True<br>|
| **static** | False |

> C++ defination code:
> ```cpp
> void reset(bool start = true)
> ```
#### record {#record}

```python
def record(*args, **kwargs)
```
Record, Read all cached data in buffer and return. If there is no audio data in the buffer, may return empty data.

| item | description |
| --- | --- |
| **type** | func |
| **note** | **1**. Do not set the time too low, for example: 1ms, as the buffer may not be ready with audio data, which could corrupt the internal state.<br>**2**. In non-blocking mode, you need to actively execute reset() before you can start capturing audio.<br>Additionally, in non-blocking mode, if the buffer does not have enough data, only the currently prepared audio data will be returned.<br>As a result, the length of the actual output audio data may not match the length of the captured audio data.<br>|
| **param** | **record_ms**: Block and record audio data lasting `record_ms` milliseconds and save it to a file, the return value does not return audio data. Only valid if the initialisation `path` is set.<br>|
| **return** | pcm data. datatype @see Bytes. If you pass in record_ms parameter, the return value is an empty Bytes object. |
| **static** | False |

> C++ defination code:
> ```cpp
> maix::Bytes *record(int record_ms = -1)
> ```
#### finish {#finish}

```python
def finish(self) -> maix.err.Err
```
Finish the record, if you have passed in the path, this api will save the audio data to file.

| item | description |
| --- | --- |
| **type** | func |
| **return** | error code, err::ERR_NONE means success, others means failed |
| **static** | False |

> C++ defination code:
> ```cpp
> err::Err finish()
> ```
#### frame\_size {#frame\_size}

```python
def frame_size(self, frame_count: int = 1) -> int
```
Returns the number of bytes for frame_count frames.

| item | description |
| --- | --- |
| **type** | func |
| **param** | **frame_count**: frame count<br>|
| **return** | frame bytes |
| **static** | False |

> C++ defination code:
> ```cpp
> int frame_size(int frame_count = 1)
> ```
#### get\_remaining\_frames {#get\_remaining\_frames}

```python
def get_remaining_frames(self) -> int
```
Return the number of frames available for reading during recording, unit is frame.

| item | description |
| --- | --- |
| **type** | func |
| **note** | The number of bytes per frame can be calculated using frame_size(). |
| **return** | remaining frames |
| **static** | False |

> C++ defination code:
> ```cpp
> int get_remaining_frames()
> ```
#### period\_size {#period\_size}

```python
def period_size(self, period_size: int = -1) -> int
```
Set/Get the audio buffer size, unit: frame.

| item | description |
| --- | --- |
| **type** | func |
| **note** | **1**. Generally, the buffer size needs to be modified during non-blocking operations.<br>**2**. The number of bytes per frame can be calculated using frame_size().<br>|
| **param** | **period_size**: When period_size is less than 0, the current value of period_size will be returned;<br>when period_size is greater than 0, period_size will be updated, and the size of period_size after setting will be returned.<br>|
| **return** | the current period size |
| **static** | False |

> C++ defination code:
> ```cpp
> int period_size(int period_size = -1)
> ```
#### period\_count {#period\_count}

```python
def period_count(self, period_count: int = -1) -> int
```
Set/Get the audio buffer count, unit: frame.

| item | description |
| --- | --- |
| **type** | func |
| **note** | Generally, the buffer size needs to be modified during non-blocking operations. |
| **param** | **period_count**: When period_count is less than 0, the current value of period_count will be returned;<br>when period_count is greater than 0, period_count will be updated, and the size of period_count after setting will be returned.<br>|
| **return** | the current period size |
| **static** | False |

> C++ defination code:
> ```cpp
> int period_count(int period_count = -1)
> ```
#### sample\_rate {#sample\_rate}

```python
def sample_rate(self) -> int
```
Get sample rate

| item | description |
| --- | --- |
| **type** | func |
| **return** | returns sample rate |
| **static** | False |

> C++ defination code:
> ```cpp
> int sample_rate()
> ```
#### format {#format-2}

```python
def format(self) -> Format
```
Get sample format

| item | description |
| --- | --- |
| **type** | func |
| **return** | returns sample format |
| **static** | False |

> C++ defination code:
> ```cpp
> audio::Format format()
> ```
#### channel {#channel}

```python
def channel(self) -> int
```
Get sample channel

| item | description |
| --- | --- |
| **type** | func |
| **return** | returns sample channel |
| **static** | False |

> C++ defination code:
> ```cpp
> int channel()
> ```
### Player {#Player}

Player class


> C++ defination code:
> ```cpp
> class Player
> ```

#### \_\_init\_\_ {#\_\_init\_\_-2}

```python
def __init__(self, path: str = '', sample_rate: int = 48000, format: Format = ..., channel: int = 1, block: bool = True) -> None
```
Construct a new Player object

| item | description |
| --- | --- |
| **type** | func |
| **param** | **path**: player path. the path determines the location where you save the file, if path is none, the audio module will not save file.<br>**sample_rate**: player sample rate, default is 48000(48KHz), means 48000 samples per second.<br>**format**: player sample format, default is audio::Format::FMT_S16_LE, means sampling 16 bits at a time and save as signed 16 bits, little endian. see @audio::Format<br>**channel**: player sample channel, default is 1, means 1 channel sampling at the same time<br>**block**: block record, default is true, means block record, if false, record will not block<br>|
| **static** | False |

> C++ defination code:
> ```cpp
> Player(std::string path = std::string(), int sample_rate = 48000, audio::Format format = audio::Format::FMT_S16_LE, int channel = 1, bool block = true)
> ```
#### volume {#volume-2}

```python
def volume(self, value: int = -1) -> int
```
Set/Get player volume

| item | description |
| --- | --- |
| **type** | func |
| **param** | **value**: volume value, If you use this parameter, audio will set the value to volume,<br>if you don't, it will return the current volume. range is [0, 100].<br>|
| **return** | the current volume |
| **static** | False |

> C++ defination code:
> ```cpp
> int volume(int value = -1)
> ```
#### play {#play}

```python
def play(self, data: maix.Bytes(bytes) = b'') -> maix.err.Err
```
Play

| item | description |
| --- | --- |
| **type** | func |
| **param** | **data**: audio data, must be raw data<br>|
| **return** | error code, err::ERR_NONE means success, others means failed |
| **static** | False |

> C++ defination code:
> ```cpp
> err::Err play(maix::Bytes *data = maix::audio::Player::NoneBytes)
> ```
#### frame\_size {#frame\_size-2}

```python
def frame_size(self, frame_count: int = 1) -> int
```
Returns the number of bytes for frame_count frames.

| item | description |
| --- | --- |
| **type** | func |
| **param** | **frame_count**: frame count<br>|
| **return** | frame bytes |
| **static** | False |

> C++ defination code:
> ```cpp
> int frame_size(int frame_count = 1)
> ```
#### get\_remaining\_frames {#get\_remaining\_frames-2}

```python
def get_remaining_frames(self) -> int
```
Return the number of idle frames available for writing during playback, unit: frame. if there are no idle frames, it will cause blocking.

| item | description |
| --- | --- |
| **type** | func |
| **note** | The number of bytes per frame can be calculated using frame_size(). |
| **return** | remaining frames |
| **static** | False |

> C++ defination code:
> ```cpp
> int get_remaining_frames()
> ```
#### period\_size {#period\_size-2}

```python
def period_size(self, period_size: int = -1) -> int
```
Set/Get the audio buffer size, unit: frame.

| item | description |
| --- | --- |
| **type** | func |
| **note** | **1**. Generally, the buffer size needs to be modified during non-blocking operations.<br>**2**. The number of bytes per frame can be calculated using frame_size().<br>|
| **param** | **period_size**: When period_size is less than 0, the current value of period_size will be returned;<br>when period_size is greater than 0, period_size will be updated, and the size of period_size after setting will be returned.<br>|
| **return** | the current period size |
| **static** | False |

> C++ defination code:
> ```cpp
> int period_size(int period_size = -1)
> ```
#### period\_count {#period\_count-2}

```python
def period_count(self, period_count: int = -1) -> int
```
Set/Get the audio buffer count, unit: frame.

| item | description |
| --- | --- |
| **type** | func |
| **note** | Generally, the buffer size needs to be modified during non-blocking operations. |
| **param** | **period_count**: When period_count is less than 0, the current value of period_count will be returned;<br>when period_count is greater than 0, period_count will be updated, and the size of period_count after setting will be returned.<br>|
| **return** | the current period size |
| **static** | False |

> C++ defination code:
> ```cpp
> int period_count(int period_count = -1)
> ```
#### reset {#reset-2}

```python
def reset(self, start: bool = False) -> None
```
Reset player status

| item | description |
| --- | --- |
| **type** | func |
| **param** | **start**: start play audio data, default is False<br>|
| **static** | False |

> C++ defination code:
> ```cpp
> void reset(bool start = false)
> ```
#### sample\_rate {#sample\_rate-2}

```python
def sample_rate(self) -> int
```
Get sample rate

| item | description |
| --- | --- |
| **type** | func |
| **return** | returns sample rate |
| **static** | False |

> C++ defination code:
> ```cpp
> int sample_rate()
> ```
#### format {#format-3}

```python
def format(self) -> Format
```
Get sample format

| item | description |
| --- | --- |
| **type** | func |
| **return** | returns sample format |
| **static** | False |

> C++ defination code:
> ```cpp
> audio::Format format()
> ```
#### channel {#channel-2}

```python
def channel(self) -> int
```
Get sample channel

| item | description |
| --- | --- |
| **type** | func |
| **return** | returns sample channel |
| **static** | False |

> C++ defination code:
> ```cpp
> int channel()
> ```
