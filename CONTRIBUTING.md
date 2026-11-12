# Contributing to TN BusConnect

Thank you for helping map **Tamil Nadu's 38-district public bus network**!  
You don't need to write HTML or JavaScript to contribute real bus timings.

---

## Option 1: Non-Coders (Submit via GitHub Issue)
1. Go to the **Issues** tab -> click **New issue**.
2. Choose **"Add or Fix Bus Timing"** (or **"Request / Add New District"**).
3. Fill in the District, From, To, exact departure times/frequency, via stops, and attach a photo of the bus stand timetable board if you have one.

---

## Option 2: Developers (Edit `data/districts.json` via Pull Request)

All bus stops, routes, schedules, and stand boards live in `data/districts.json`.

### Route Entry Format
```json
"nkl->mohanur": [
  {
    "time": "05:30 – 21:30",
    "eta": "Every 15–20m",
    "title": "Town Bus Rt 9 (SH-95)",
    "type": "town",
    "vetri": true,
    "corp": "TNSTC Salem",
    "bay": "Namakkal Old / New Stand",
    "via": "Aniyapuram · Keerambur · Parali · Mohanur (~19 km)",
    "fare": "₹12 – ₹15",
    "dur": "30–40 min",
    "gps": false,
    "source": "General Frequency"
  }
]
```

### Rules for Data Quality
1. **No guessed/fake data:** Only add timings verified from official TNSTC/MTC boards, `tnstc.in`, or direct physical bus stand timetables.
2. **Include both directions:** Add both `from->to` and `to->from` so the Reverse (`⇅`) button works accurately.
3. **Vetri Payanam flag:** Set `"vetri": true` only for eligible ordinary town/city buses.
4. **Test locally** before opening a PR:
   ```bash
   python -m http.server 8080
   # Open http://localhost:8080
   ```
