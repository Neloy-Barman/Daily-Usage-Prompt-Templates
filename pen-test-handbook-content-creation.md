``````md
## CONTEXT
I am learning the `Phases of Penetration Testing`. There I find different commands and implementing those I understand how it works. Now I want to make a cheatsheet to use it as a handbook for future. I will provide with the implemented command or a series of commands that I learnt as data. You need to generate a title for the task that can be done using the command, a generic command by replacing specific IP/host/port values with placeholders (e.g., `<target_ip>`, `<host>`, `<port>`), and add details of flags being used. You also need to analyze and briefly describe the expected output when the command runs successfully and when it fails. Also add the use cases defining when the user should use the command(s). Return the data in `.md` tabular format.

## EXAMPLE COMMAND DATA
```md
    <example_command_data>
```

## TASK
Generate `Task Title`, `Command`, `Flag Details`, `Output on Pass & Fail` and `Usecase` for the the given data and return the data with `.md` tabular format. 

## RULES
- The `Task Title` should be `Relevant` and `Descriptive and Action-Oriented`.
- Create generic commands by replacing specific values (host, target, port) with descriptive placeholders like `target_ip` or `port_number`.
- Add details in short for the flags, so that one can understand easily the purpose of using the flag and use it when required.
- Describe typical success and error messages in 1-2 sentences each for both pass and fail scenarios.
- In `Usage` part, add scenarios, when one should use the command to achieve goal.
- If multiple commands are given, then use line breaking to seperate the data within the same column for example, ```<cmd_1>```<br>```<cmd_2>```<br>... . Perform the same thing for the examples too.
- If command syntax is invalid, note this in the Flag Details column.
- Use Markdown elements as needed, such as `bold text`, `lists` and `break line`.
- In `lists`, bold `key terms` or `labels` that appear before a colon.
- The sentences should be `Concise`, `Easy`, `Clean` and in `Beginner-friendly` tone.
- Use common penetration testing terminology appropriate for beginners.
- The content should be `To the point`.
- Return me with the whole response as a `Markdown` within **4 Backticks**(````<generated_markdown_content>````).
- Strictly keep the generated content within **4 Backticks**.

## EXAMPLE
### Example 1
INPUT: 
```md
    nmap -sS -Pn 172.16.32.131
```
OUTPUT:
````md
| **Stealth SYN Scan (Skip Ping)** | ```nmap -sS -Pn target_ip``` | ```nmap -sS -Pn 172.16.32.131``` | **1. -sS (TCP SYN Scan):** Sends a SYN packet (half-open connection). It does not complete the TCP handshake, making it faster and less likely to be logged by older firewalls.<br>**2. -Pn (No Ping):** Skips the host discovery phase. Tells Nmap to assume the host is online and scan the ports immediately.| **Pass:**<br>A list of discovered ports with columns: `PORT`, `STATE` (Open/Filtered), and `SERVICE`.<br>**Fail:**<br>1. `Requested scan type which requires root privileges` (If run without sudo).<br>2. Note: `Host seems down` (Only if the IP is truly offline or routing fails, though -Pn tries to force it).| **Phase:** Scanning & Enumeration.<br>**Use when:**<br>1. You suspect a firewall is blocking ICMP (Ping) requests.<br>2. You want a fast scan that is "quieter" than a full TCP connect scan.|
````
### Example 2
INPUT: 
```md
    /etc/init.d/postgresql start
    msfconsole
    db_connect postgres:toor@127.0.0.1/msfbook
    db_status
```
OUTPUT:
````md
| **Initialize Metasploit Database: Start PostgreSQL, Launch msfconsole, Connect, and Verify** | ```/etc/init.d/postgresql start```<br>```msfconsole```<br>```db_connect db_user:db_pass@db_host:db_port/db_name```<br>```db_status``` | ```/etc/init.d/postgresql start```<br>```msfconsole```<br>```db_connect postgres:toor@127.0.0.1/msfbook```<br>```db_status``` | - **postgresql start:** Starts the PostgreSQL service. Requires root privileges; use sudo if needed.<br>- **msfconsole:** Launches Metasploit’s interactive console. No flags used here (common optional: -q quiet, -r rc_file).<br>- **db_connect:** Connect to a DB. Format: `user:pass@host:port/dbname` (default Postgres port is 5432). Uses Postgres by default in MSF.<br>- **db_status:** Shows current DB connection state inside msfconsole. | - **postgresql start – Pass:** Prints “Starting PostgreSQL…” or service “active (running)”.<br>**postgresql start – Fail:** “Failed to start postgresql.service” or “Permission denied” (try sudo) / service not found.<br>- **msfconsole – Pass:** Metasploit banner appears and you get an `msf6 >` prompt.<br>**msfconsole – Fail:** “msfconsole: command not found” or dependency errors preventing startup.<br>- **db_connect – Pass:** “Connected to <db_name>. Connection type: postgresql.”<br>**db_connect – Fail:** “password authentication failed for user …” or “could not connect to server: Connection refused/timeout”.<br>- **db_status – Pass:** “Connected to <db_name>. Connection type: postgresql.”<br>**db_status – Fail:** “No database connection” or “Disconnected”. | - **Phase:** Environment Setup & Data Management.<br>- **Use when:**<br>  - **Before recon/enumeration:** You want results (hosts, services, creds) saved in the MSF DB.<br>  - **After fresh install/reboot:** Start Postgres and verify MSF can talk to it.<br>  - **If modules seem slow/disconnected:** Reconnect the DB to speed up searches and caching.<br>  - **When importing/exporting data:** Use DB-backed workspaces for persistence across sessions. |
````

## RESPONSE RETURN FORMAT
````md
| **<task_title>** | ```<generic_command>``` | ```<example_command>``` | <flag_details> | <pass_&_fail_output> | <when_to_use> |
````
``````

# Expected Response from LLMs & Platforms

- **LLM**: `gpt-5.1-high`<BR>**Platform**: `https://lmarena.ai/`
- **LLM**: `gpt-5-high-new-system-prompt`<BR>**Platform**: `https://lmarena.ai/`