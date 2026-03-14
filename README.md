# Robotics Deployment & QA — Assignment Submission

## Submitted Files

| File | Description |
|------|-------------|
| `Robotics_QA_Assignment.docx` | Complete written assignment — Part 1 analysis, Part 2 DOE, Part 3 Bug Report |
| `analyze_robot_log.py` | Python script for Part 1 — log parsing, stall counting, pressure analysis, correlation |
| `README.md` | This file |

---

## How to Run the Script

### Requirements
- Python 3.10 or higher
- No external libraries needed (uses built-in `csv` module only)

### Run
```bash
python analyze_robot_log.py
```

### With the real log file (if available)
Place `robot_state_log.csv` in the same folder as the script, then run:
```bash
python analyze_robot_log.py
```
The script will automatically detect and use the CSV file instead of the embedded sample data.

---

## Expected Output

```
🤖  ROBOT STATE LOG ANALYZER
    Deployment & QA Assignment — Part 1

REQUIREMENT 1: ERR_SANDER_STALL Count
  Total rows flagged ERR_SANDER_STALL : 2
  Unique stall events (onset count)    : 1

REQUIREMENT 2: Avg Arm Pressure 1.0s Before Each Stall
  Stall onset @ t=1005.3s
    Avg pressure (kg)  : 4.14
    Peak pressure (kg) : 6.20

REQUIREMENT 3: Correlation / Variable Analysis
  base_speed_ms    +75.8%  ⚠️  SIGNIFICANT
  target_rpm       -29.3%  ⚠️  SIGNIFICANT
  actual_rpm       -47.4%  ⚠️  SIGNIFICANT
  arm_pressure_kg  +77.6%  ⚠️  SIGNIFICANT
```

---

## Notes
- Sample log data from the assignment PDF is embedded directly in the script
- All three parts of the assignment are fully addressed in the Word document
