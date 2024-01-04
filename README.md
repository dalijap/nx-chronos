# NX Chronos - Chronometer for Delphi

## Features

Cross-platform stopwatch with similar functionality to `TStopwatch`, but it
allows measuring different times: real time, process time, and thread time,
including highly accurate process cycles and thread cycles. 

If you are measuring cycles, you will only be able to get a raw `Elapsed` value
that cannot be converted to nanoseconds, milliseconds, or seconds. 

`ProcessCycles` and `ThreadCycles` measuring modes are supported only Windows
Vista and newer OS.

## Supported platforms

  + NX Chronos is platform-agnostic and is supported on all available platforms
  + Tested on: XE4, 10.3.3 Rio, 10.4.2 Sydney, and 11.3 Alexandria, but it should work on 
    other versions between XE4 and the current version using classic compiler.

## Basic usage

```delphi
var
  ts: TNxChronometer;
begin
  ts := TNxChronometer.Start(ProcessTime);
  // code to be measured
  ...
  ts.Stop;
  Writeln('Process time: ', ts.ElapsedMs);
end;
```


---

[https://dalija.prasnikar.info](https://dalija.prasnikar.info)

