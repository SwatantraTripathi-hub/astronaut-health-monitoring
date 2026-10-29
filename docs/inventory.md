# Data inventory

Only what I actually opened and saw. Anything unchecked says "not checked".

| Dataset | Record | Signals | Units | Fs (Hz) | Duration | Labels | Odd / missing | License |
|---|---|---|---|---|---|---|---|---|
| MIT-BIH | 100 | MLII, V5 | mV | 360 | 1805.6 s | beat + rhythm (.atr) | `A` beat at ~4.5 s (meaning: verify in docs) | ODC-By 1.0 per PhysioNet page |
| MIT-BIH | 201 | MLII, V1 | mV | 360 | 1805.6 s | beat + rhythm (.atr) | irregular RR but all `N` in first 10 s | same |
| BIDMC | bidmc01 | RESP, PLETH, V, AVR, II (names have trailing commas) | pm, NU, mV | 125 | 480.0 s | breath annotations (.breath) | names have commas | read `LICENSE` file and fill in |
| BIDMC | bidmc01n | HR, PULSE, RESP, SpO2 | bpm, bpm, pm, % | 1 | 481 s | none | numerics RESP is not the waveform RESP | same as above |

## Byte-size checks
- bidmc01.dat: 5 signals x 60,001 samples x 2 bytes = 600,010 (matches file size)
- 100.dat: 650,000 samples x 2 channels x 1.5 bytes = 1,950,000 (matches file size)

## Not yet checked
- OSD-343 file contents
- BIDMC license name (read LICENSE file)
- Meaning of beat symbol `A` (MIT-BIH docs)
- What the `+` rhythm notes say for records 100 and 201