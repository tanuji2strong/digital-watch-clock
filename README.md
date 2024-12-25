# digital-watch-clock

# FPGA Digital Clock Documentation

## 1. Introduction
A digital clock implemented on an FPGA using Verilog, featuring time tracking (seconds, minutes, hours), manual adjustments, and a beeper.

## 2. System Overview
- **Clock Frequency:** 50 MHz
- **Display:** 4-digit Seven-Segment Display
- **Controls:** Hour (btnL), Minute (btnU)
- **Beeper:** Hourly notification pulse

## 3. Modules
- **Counter:** Tracks time, handles manual adjustments, and triggers the beeper.
- **Seven-Segment Display:** Multiplexes digits for time display.
- **Clock Divider:** Generates 200 Hz clock for display refresh.
- **Top Module:** Integrates all modules.

## 4. Key Signals
| Signal | Description |
|--------|-------------|
| clk    | System clock (50 MHz) |
| btnU   | Adjust minutes |
| btnL   | Adjust hours |
| led    | Seconds counter |
| seg    | 7-segment segments |
| an     | Active digit control |
| dp     | Decimal point |
| beeper | Hourly pulse |

## 5. Beeper
- Activates for 0.5 seconds every hour change.

## 6. Design Notes
- Assumes a 50 MHz clock.
- Manual buttons require external debouncing.
- Display refresh at 200 Hz.

## 8. Conclusion
This FPGA-based clock demonstrates modular design, precise timekeeping, and user interactivity.

**End of Documentation**

