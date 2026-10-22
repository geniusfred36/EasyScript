# EasyScript

EasyScript is a beginner-friendly, command-based scripting language with its own interpreter. It is designed to make small scripts and automation tasks approachable without requiring users to write Python syntax. EasyScript programs use the `.easy` file format and are interpreted by the EasyScript runtime.

## Features

- Readable command-style scripting syntax
- Expressions, variables, conditional logic, loops, and user-defined functions
- Built-in utilities for text, collections, mathematics, dates, and time
- File and folder operations, JSON support, and regular-expression helpers
- Networking utilities such as DNS lookup, TCP checks, URL helpers, and HTTP requests
- Authenticated remote listing, reading, writing, and editing of `.easy` files
- Compatibility with selected commands from earlier EasyScript and DuckyScript versions where practical

The remote file service is designed for file operations; it does not execute code received from a remote client. Network and file features can still affect your computer or network, so only run scripts you trust and only connect to systems you are authorized to access.

## Run EasyScript

### Windows executable

Start the interactive prompt:

```powershell
EasyScript.exe
```

Run a script:

```powershell
EasyScript.exe path\to\script.easy
```

### Python source

If you are using the Python source instead of the Windows executable, run it with Python 3:

To open the interactive prompt, run:

```powershell
py EasyScript_1.0.3.py
```

Some optional keyboard-control commands depend on the optional `pyautogui` package and may require additional operating-system permissions.

## Project status

EasyScript is a custom scripting-language project. Features and command compatibility may change between versions. Check the release notes for the version you are using.

## Copyright and permissions

Copyright © 2026 Geniusfred36. All rights reserved.

EasyScript is proprietary software and is not released under an open-source license. You may not copy, modify, redistribute, sublicense, or create derivative works of the EasyScript interpreter without prior written permission from the copyright holder, except where permitted by applicable law.

You are welcome to create your own `.easy` scripts, compatible tools, add-ons, tutorials, and other independent projects for use with EasyScript. These projects must not improperly include or redistribute the proprietary EasyScript source code.

Please credit Geniusfred36 when referring to the official EasyScript project. Permission to create independent projects does not grant permission to copy or modify the EasyScript interpreter itself.
