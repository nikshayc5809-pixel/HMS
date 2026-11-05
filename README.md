# Hotel Management System (CLI)


A lightweight, console-based hotel management application written in C. It enables front-desk operations such as registering guest check-ins, processing checkouts, tracking remaining reservation days in real time, and maintaining persistent records via binary file storage.

---

## Features

- **Guest Check-in (`Add Guest`)**: Captures guest name, room number, total booking duration, and sets an automatic timestamp for check-in using `time.h`.
- **Guest Checkout (`Remove Guest`)**: Checks out guests by room number and adjusts existing records dynamically.
- **Real-Time Booking Status (`Show Booking Times`)**: Calculates elapsed time against check-in timestamps to report remaining days.
- **Guest Directory (`Show All Guests`)**: Lists all currently checked-in guests alongside room assignments and durations.
- **Data Persistence**: Automatically reads from and writes to `guests.dat` using binary file I/O (`fread`/`fwrite`), ensuring records persist across restarts.
- **Input Validation**: Sanitizes non-integer inputs to prevent buffer overflows and infinite loop crashes.

---

## Technical Specifications

| Parameter | Value |
|---|---|
| **Language** | C (C99 or newer recommended) |
| **Capacity** | Fixed limit of 50 concurrent guests (`MAX_GUESTS 50`) |
| **Storage Engine** | Binary file (`guests.dat`) |
| **Time Tracking** | Unix epoch timestamps (`time_t`) |

---

## Project Structure

```text
.
├── main.c          # Core program source code
├── guests.dat      # Binary database file (auto-generated on first save)
└── README.md       # Project documentation
