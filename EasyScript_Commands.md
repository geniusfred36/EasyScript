# EasyScript 1.0.3 — Command Reference

This reference is based on the EasyScript 3.2 English source. EasyScript supports both **bracket-style statements** such as `TEXT["Hello"]` and **functions inside expressions** such as `upper("hello")`.

## 1. Basic commands and variables

- `TEXT[expression]` — print text or a value.
- `EVAL[expression]` — evaluate an EasyScript expression.
- `INPUT["Prompt"]` or `input("Prompt")` — ask the user for input.
- `name = expression` — create or update a variable. `+=`, `-=`, `*=`, `/=`, and `%=` update an existing value.
- `VARS` — show current variables.
- `GET[name]` — display a variable's value.
- `SET[name, value]` — create or update a variable.
- `DELVAR[name]` — delete a variable.
- `HELP` — show the built-in help.
- `CLEAR` / `CLS` — clear the console.
- `EXIT` / `QUIT` — leave the interactive interpreter.

## 2. Flow control and functions

- `IF[condition] ... ELIF[condition] ... ELSE ... ENDIF` — conditional logic.
- `WHILE[condition] ... ENDWHILE` — repeat while a condition is true.
- `FOR[item, count] ... ENDFOR` — iterate a number of times or over an iterable.
- `FOR[item, start, stop, step] ... ENDFOR` — iterate through a numeric range; the stop value is exclusive.
- `FOREACH[item, list] ... ENDFOREACH` — iterate over a collection.
- `FUNCTION[name, parameter1, parameter2] ... RETURN[expression] ... ENDFUNCTION` — define a function and return a value.
- `TRY ... CATCH[error] ... FINALLY ... ENDTRY` — handle errors and run cleanup code.
- `BREAK` / `STOPLOOP` — exit the current loop.
- `CONTINUE` / `NEXTITERATION` — skip to the next loop iteration.
- `RETURN[expression]` — return from a function.
- `ASSERT[condition, message]` / `assert_true(condition, message)` — raise an error if a check fails.
- `RAISE[message]` / `error(message)` — raise an EasyScript error.

## 3. Collections and data manipulation

Bracket-style commands:

- `SETITEM[collection, key, value]` — set a list or dictionary item.
- `DELITEM[collection, key]` — delete an item.
- `APPEND[list, value]` — append an item.
- `INSERT[list, position, value]` — insert an item at a position.
- `POP[list]` — remove and return an item.
- `REMOVE[list, value]` — remove a matching value.
- `SORT[list]` / `REVERSE[list]` — sort or reverse a list.

Collection functions: `list`, `tuple`, `dict`, `set`, `frozenset`, `len`, `sorted`, `reversed`, `range`, `enumerate`, `zip`, `any`, `all`, `contains`, `keys`, `values`, `items`, `get`, `has_key`, `set_item`, `delete_item`, `append`, `extend`, `insert`, `pop`, `remove`, `clear`, `copy`, `index`, and `count`.

## 4. Numbers and types

- Conversion and inspection: `str`, `int`, `float`, `bool`, `type`, `isinstance`, `issubclass`, `complex`, `bytes`, `bytearray`, `memoryview`, `hash`, `id`, `callable`, `iter`, `next`, `slice`, `repr`, `ascii`, `format`, `bin`, `oct`, `hex`, `ord`, and `chr`.
- Basic calculations: `abs`, `round`, `min`, `max`, `sum`, `pow`, `divmod`, `trunc`, `copysign`, `fsum`, `prod`, `comb`, `perm`, `gcd`, `lcm`, `isclose`, `isfinite`, `isinf`, `isnan`, `isqrt`, and `hypot`.
- Maths: `sqrt`, `floor`, `ceil`, `sin`, `cos`, `tan`, `asin`, `acos`, `atan`, `atan2`, `degrees`, `radians`, `log`, `log10`, `exp`, `factorial`, and `clamp`.
- Utilities for inspecting names and scopes: `dir`, `globals`, `locals`, and `vars`.

Expressions support numbers, strings, `True`, `False`, `None`, arithmetic, comparisons, `AND`, `OR`, `NOT`, lists, dictionaries, indexing, and slicing.

## 5. Text and strings

`upper`, `lower`, `title`, `capitalize`, `casefold`, `strip`, `lstrip`, `rstrip`, `replace`, `split`, `join`, `startswith`, `endswith`, `find`, `rfind`, `count_text`, `isdigit`, `isalpha`, `isalnum`, `isspace`, `center`, `ljust`, `rjust`, and `zfill`.

## 6. Random values, dates, and time

- Random: `random`, `randint`, `uniform`, `choice`, `sample`, `shuffle`, and `seed`.
- Date and time: `today`, `now`, `clock`, `timestamp`, `date_format`, and `sleep`.

## 7. Files and paths

Bracket-style commands:

- `READ[file]` — display a text file's contents; it can also be used in an assignment such as `contents = READ["file.txt"]`.
- `WRITE[file, text]` — overwrite a file.
- `WRITE[file, +, text]` — append a line.
- `WRITE[file, -1, text]` — replace line 1; use another negative line number for another line.
- `WRITE[file, -showall]` — display a file with line numbers.
- `RUN[file]` — run another EasyScript script.
- `DEL[file]` / `DELETE[file]` — delete a file.
- `MKDIR[folder]` — create a folder.

File and path functions: `exists`, `is_file`, `is_dir`, `listdir`, `mkdir`, `read_text`, `write_text`, `append_text`, `remove_file`, `copy_file`, `move_file`, `basename`, `dirname`, `join_path`, `abspath`, `cwd`, and `filesize`.

## 8. JSON and regular expressions

- `JSON[value]` or `JSON[value, pretty]` — print JSON.
- `json_parse(value)` — parse JSON text into data.
- `json_stringify(value, pretty)` — convert data into JSON text.
- `regex_search(pattern, text)` — check whether a pattern occurs.
- `regex_match(pattern, text)` — check whether the whole text matches.
- `regex_findall(pattern, text)` — find all matches.
- `regex_replace(pattern, replacement, text)` — replace matches.

## 9. HTTP and networking

- `DNS[host]` / `DNS_LOOKUP[host]` or `dns_lookup(host)` — look up a hostname.
- `HOSTNAME()` — return the computer name.
- `LOCAL_IP()` / `local_ip()` — return the local network address selected for a route.
- `TCP_CHECK[host, port, timeout]` / `tcp_check(host, port, timeout)` — check whether a TCP port can be reached.
- `HTTP_GET[url, timeout, headers]` / `http_get(url, timeout)` — send an HTTP GET request.
- `HTTP_POST[url, body, content_type, timeout, headers]` / `http_post(...)` — send data with HTTP POST.
- `HTTP_REQUEST[url, method, body, headers, timeout]` / `http_request(...)` — make an HTTP request and return status, headers, and body. Supported methods are GET, POST, PUT, PATCH, DELETE, and HEAD.
- URL helpers: `url_encode`, `url_decode`, `url_join`, and `url_query`.
- IP helpers: `is_ip`, `ip_version`, `ip_private`, and `ip_public`.

## 10. Authenticated remote `.easy` file editing

- `REMOTE_SERVER[port, secret, shared_folder]` — start the file server on the computer hosting the shared `.easy` files. The folder defaults to `EasyShared`.
- `REMOTE_LIST[host:port, secret, folder]` — list remote shared files.
- `REMOTE_READ[host:port, secret, file.easy]` — read a remote script.
- `REMOTE_WRITE[host:port, secret, file.easy, content]` — create or overwrite a remote script.
- `REMOTE_EDIT[host:port, secret, file.easy]` — edit a local copy and sync it back.
- `REMOTE_EDIT[host:port, secret, remote.easy, local.easy]` — specify the local copy filename.

Use a strong secret of at least 16 characters and only on a trusted network. Do not expose the service through router port forwarding. The remote file server handles `.easy` files; it does not execute code received from remote clients.

## 11. System and compatibility commands

- `CMD[command]` — launch a system-shell command.
- `PING[host]` — ping a host.
- `IPCONFIG` — show network configuration.
- `WHOAMI` — show the current system user.
- `TIME` / `DATE` — show the current time or date.
- `SYSINFO` — show basic operating-system and machine information.
- `DIR` — list files in the script's directory.
- `TYPE[text]` — type text using keyboard automation.
- `PRESS[key]` — press a key using keyboard automation.
- `SLEEP[seconds]` / `sleep(seconds)` — pause execution.
- `SERVER[port]` and `SEND[host:port, command]` — legacy TCP controller/target commands; use with care and only in a trusted environment.

## 12. DuckyScript-compatible keyboard commands

These commands are supported for compatible `.txt`/`.duck`/`.easy` scripts: `STRING`, `DELAY`, `REM`, `#`, `ENTER`, `TAB`, `SPACE`, `ESCAPE`, `BACKSPACE`, `DELETE`, `UP`, `DOWN`, `LEFT`, `RIGHT`, `HOME`, `END`, `GUI`, `WINDOWS`, `CTRL`, `CONTROL`, `ALT`, and `SHIFT`.

Keyboard automation requires the optional `PyAutoGUI` dependency. Without it, key presses and typing are not performed.

## Important notes

- EasyScript uses its own expression parser. `EVAL[...]` evaluates EasyScript expressions; it does **not** execute Python source code.
- Some older commands are retained for compatibility with previous EasyScript versions.
- Commands that modify files, launch shell commands, or send keyboard input can affect the computer running them. Review scripts before running them.
