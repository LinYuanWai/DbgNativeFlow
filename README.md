⭐ DbgNativeFlow — Enhanced Native Toolkit for x64dbg
A lightweight, high‑performance extension suite for real‑world reverse engineering.

🔧 Overview
DbgNativeFlow is a collection of native x64dbg extensions designed for practical reverse engineering workflows.
No dependencies, no scripting frameworks, no heavy UI layers — just pure C++ and Win32 API fast, predictable behavior.

The goal is simple:

Make x64dbg smoother, faster, and more capable, without changing how you normally debug.

All features integrate directly into the CPU window’s right‑click menu, so you never lose context or switch views.

🚀 Key Features
⚡ High‑performance ListView (2–5 million rows)
Custom‑built virtual ListView

Instant UI response, no stutter

Non‑recursive quicksort using a simulated stack

Sorts 100k rows instantly; millions in a background thread

Every column is sortable

📁 Universal Export
All results can be exported as comma‑separated text (Excel‑compatible) or binary files.

💾 Persistent Results
Every module:

Saves results automatically

Restores them on next launch

Recalculates addresses automatically

🧩 Included Modules (CPU Window → DbgNativeFlow)
1. Find Text
Search assembly instructions across one or multiple modules.

Supports:

Plain text (call, Create, #20, etc.)

Cross‑module API call discovery

Reverse‑tracing workflows (e.g., encryption routines)

2. Find Call
Same as Find Text, but limited to branch instructions (call, jmp, etc.).

3. Search Strings
Search static module strings or dynamic memory strings.

Supports:

ASCII

GBK

Unicode

UTF‑8

Memory strings can be hardware‑breakpointed to find who reads sensitive data (passwords, tokens, etc.).

4. Search Binary
Binary pattern search with wildcards (* or ? per byte).
More flexible and readable than x64dbg’s built‑in signature search.

5. Window Message Monitor
x64dbg cannot capture window messages from the debuggee — this module fixes that.

Features:

5 types of Windows hooks

Capture mouse, keyboard, and window messages

Right‑click to set precise breakpoints on specific messages

Exclusion list (e.g., hide WM_MOUSEMOVE, WM_TIMER)

6. Trace Record
Enhanced version of x64dbg’s Trace:

Shows all 16 registers for every instruction

More readable

Stops safely on async failures

Ideal for controlled start/end tracing

7. Breakpoint Record
A lightweight alternative to Trace.

Records:

Every breakpoint hit

In exact order

With full register context

Perfect for analyzing algorithms step‑by‑step.

8. Breakpoint List
Manage all breakpoints created by the plugin (does not affect F2 breakpoints).

9. Set Breakpoints
Quickly set breakpoints on the current CPU address.
Stored in the plugin’s breakpoint list.

10. Address Converter
Bidirectional address translation between IDA static addresses and x64dbg dynamic addresses.

Supports:

Function start detection

Module base recalculation

Copy/Follow/Breakpoint actions

Perfect for IDA pseudocode navigation

11. Script Editor
A lightweight script editor embedded inside x64dbg.

Features:

Syntax highlighting

IntelliSense

Script breakpoints

Multiple script tabs

Run single commands or full scripts instantly

🧩 Dump Window Extensions
1. Dump as C Array
Convert selected memory into a ready‑to‑use C array.
Perfect for crypto debugging and algorithm verification.

2. Follow in Dump (1–5)
Interpret the first 4/8 bytes as a pointer and jump through nested structures instantly.

📦 Installation
Unzip DbgNativeFlow.rar and copy the files into:

Code
x64dbg\plugins\release\x64\   (for 64‑bit)
x64dbg\plugins\release\x32\   (for 32‑bit)
Required files:

64‑bit
DbgNativeFlow.dp64

DbgbaseHook64.dll

32‑bit
DbgNativeFlow.dp32

DbgbaseHook32.dll

DbgbaseHook*.dll is required for Window Message Monitor (Windows hook library. Written by myself, not by a third party.)

All other modules work without it.

Optional directories:

\param\icon\         (menu icons)

\param\config\WM_Message.ini

\param\config\DbgCommand.ini

❤️ Support the Project
If this toolkit saves you time, helps your workflow, or simply makes debugging more enjoyable,
consider buying me a coffee:

👉 https://Ko-fi.com/hexhunterdev

Your support helps me continue improving the plugin.

📜 License
MIT License (or whichever you prefer)
