# Monitored items

The template uses numeric Delta UPSv5 OIDs below `1.3.6.1.4.1.2254.2.5`.

## Inventory

- Manufacturer and UPS model
- UPS firmware version
- InsightPower agent version
- Rated apparent power

## Input

- L1 frequency
- L1 voltage
- Configurable voltage and frequency thresholds

## Output

- Current power source
- Frequency
- L1 voltage
- L1 current
- L1 active power
- L1 load percentage

## Battery

- Condition: good, weak, or replace
- Status: normal, low, or depleted
- Charge state and charge mode
- Seconds on battery
- Estimated runtime
- Positive battery voltage
- Positive battery capacity

## Diagnostics and alarms

- Last self-test result and details
- Alarm summary
- Input outside tolerance
- Low battery
- Output overload
- Charger failure
- Fan failure
- Output off
- Abnormal internal temperature

## Default macros

| Macro | Default | Purpose |
|---|---:|---|
| `{$UPS.BATTERY.CAPACITY.MIN}` | 30 | Minimum battery capacity (%) |
| `{$UPS.INPUT.FREQ.MIN}` | 57 | Minimum input frequency (Hz) |
| `{$UPS.INPUT.FREQ.MAX}` | 63 | Maximum input frequency (Hz) |
| `{$UPS.INPUT.VOLTAGE.MIN}` | 198 | Minimum input voltage (V) |
| `{$UPS.INPUT.VOLTAGE.MAX}` | 242 | Maximum input voltage (V) |
| `{$UPS.LOAD.WARN}` | 80 | Load warning threshold (%) |
| `{$UPS.LOAD.HIGH}` | 95 | Critical load threshold (%) |
| `{$UPS.RUNTIME.MIN}` | 15 | Minimum runtime while on battery (minutes) |

Only OIDs that returned usable values on the validation device were included. Unsupported and NULL-returning OIDs were intentionally omitted.
