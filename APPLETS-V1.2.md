# Mono v1.2 Applet Ideas

Approved applets for future development. Each includes a Claude prompt for implementation.

---

## Utility

### Unit Converter
**Convert anything to anything**

Support length (in/cm/m/ft), weight (lb/kg/oz), temperature (F/C/K), and volume (cups/ml/L). Use a segmented picker for category, two text fields for input/output with unit dropdowns. Store last-used category. Follow Mono's monochrome aesthetic with SF Mono font.

### Tip Calculator
**Split bills without the mental math**

Fields: bill amount (currency input), tip percentage (15/18/20/25 presets + custom), split count (1-20 stepper). Display tip amount, total, and per-person amount. Animate number changes. Save preferred tip % to UserDefaults. Monochrome UI.

### Counter
**Tap to count anything**

Large centered number display (biggest font possible). Tap anywhere to +1, long press to -1. Buttons for +/- and reset. Optional: multiple named counters saved to FileState. Haptic feedback on tap. Minimal UI - the number IS the interface.

### Parking
**Never forget where you parked**

Save current location with one tap. Show distance and heading to saved location. Optional parking meter timer with notification when expiring. Add notes field for level/section. Open in Maps for directions. Uses CoreLocation. Monochrome with accent for timer warning.

### Level
**Perfectly straight, every time**

Use CoreMotion accelerometer data. Two modes: surface level (phone flat) and edge level (phone on edge). Show bubble that moves with tilt. Display degrees. Green checkmark + haptic when within 0.5 degrees of level. Lock reading button. Minimal black/white design.

---

## Health & Wellness

### Water Tracker
**Stay hydrated, simply**

Display water drops or glasses as visual progress (filled vs empty). Tap to add one glass. Daily goal setting (default 8). Resets at midnight. Store history for past 7 days with simple chart. FileState persistence. Optional reminder notifications.

### Mood Log
**One emoji, once a day**

5 emoji options (or custom set). One entry per day. Calendar view showing mood history. Monthly summary. No text required, just tap an emoji. FileState storage. Export as CSV. Respect the simplicity - don't over-feature it.

### Medication
**Did you take your meds?**

Add medications with optional time. Daily checklist that resets. Streak counter for consistency. Optional reminder notifications per medication. Simple - not a full pharmacy app, just a daily checkbox. FileState persistence. Secure with no health data export.

---

## Astronomy

### Moon Phase
**What's the moon doing tonight?**

Calculate moon phase astronomically (no API needed). Show current phase with appropriate moon emoji or custom drawn phase. Display illumination %, phase name, and dates for next full/new moon. Optional: moonrise/moonset times using location. Elegant dark UI.

### Sunrise/Sunset
**Daylight hours at a glance**

Calculate times astronomically using location + date. Show sunrise, sunset, daylight duration. Progress bar showing current time within daylight. Golden hour and blue hour times for photographers. Civil/nautical/astronomical twilight in settings. Offline calculation.

---

## Time & Date

### Date Calculator
**Days between any two dates**

Two date pickers. Show difference in days, weeks, months, and years. 'Today' quick button. Swap dates button. Add/subtract days from a date mode. Save favorite calculations (birthday countdown, etc). Clean date picker UI.

---

## Fun & Games

### Dice Roller
**D4 to D20 and beyond**

Standard RPG dice: D4, D6, D8, D10, D12, D20, D100. Big result display. Roll animation. Shake to roll. Multi-dice: 2D6, 3D8, etc. Roll history. Custom dice (D3, D30). Sum display for multiple dice. Sound toggle. Fun but minimal.

### Metronome
**Keep perfect time**

BPM control (30-240). Tap tempo button to set by tapping. Time signature selection (4/4, 3/4, 6/8). Visual beat indicator. Accent on first beat option. Tick sound (customizable). Background audio. Haptic option. Tempo presets (Largo, Adagio, etc).

### Sudoku
**Classic number puzzle**

Generate puzzles at Easy/Medium/Hard/Expert. Clean 9x9 grid. Tap cell, tap number. Notes mode for candidates. Highlight conflicts. Undo stack. Auto-save progress. No forced timers. Dark monochrome grid aesthetic. Generate puzzles algorithmically, not from database.

### 2048
**Swipe, merge, reach 2048**

4x4 grid. Swipe gestures to slide tiles. Merge matching numbers. Score tracking. High score persistence. Game over detection. New game button. Smooth tile animations. Monochrome with number-based shading (higher = more contrast). Haptics on merge.

---

## Developer Tools

### Color Picker
**HEX, RGB, HSL - convert and save**

Color wheel or slider input. Text input for HEX/RGB/HSL. Live conversion between formats. Tap to copy any value. Save colors to palette. Name saved colors. Color harmonies (complement, triadic). Eyedropper from photos. Useful for designers, minimal UI.

### Word Count
**Paste text, get stats**

Large text input area. Live counting as you type/paste. Show: words, characters (with/without spaces), sentences, paragraphs, reading time (avg 200 wpm). Clear button. Copy stats. Useful for writers hitting word limits. Clean text editor aesthetic.

### Case Converter
**Transform text case instantly**

Input text field. Buttons for: UPPERCASE, lowercase, Title Case, Sentence case, camelCase, snake_case, kebab-case, CONSTANT_CASE. Show result below with copy button. Preserve original, show converted. Swap input/output. Developer-friendly tool.

### Password Generator
**Strong passwords, instantly**

Configurable length (8-64). Toggle: uppercase, lowercase, numbers, symbols. Exclude ambiguous chars option (0/O, 1/l). Generate button. One-tap copy. Password strength indicator. Recent passwords list (local only). Never send passwords anywhere. Secure, minimal.

### QR Generator
**Turn text into scannable codes**

Text input for any content. Live QR preview using CoreImage. Presets: URL, WiFi, Contact (vCard), Plain text. Share/save QR as image. History of generated codes. Pairs with existing QR Scanner applet. Monochrome QR with optional accent color.

---

## Implementation Notes

- All applets should follow Mono's monochrome aesthetic
- Use SF Mono font where appropriate
- Persist state using FileState where noted
- Support both light and dark appearances
- Haptic feedback for interactions
- No external API dependencies where possible (offline-first)
