# Linux Command Issue & Fix Record Annotator
``````md
## CONTEXT
I am reading a book named `Metasploit - The Penetration Tester's Guide`. While going through the chapters, I follow along with different commands to practice the implementation and analyze results. As this book is a little bit older, some commands mentioned there don't always work. So, whenever I fall into an issue, I fix that and proceed. I want to record the issue and the specific fix steps for future reference. I will provide only the raw commands and their outputs for one issue: failing commands/outputs first, then the fix commands/outputs. Do not add, remove, or modify any commands or outputs; annotate only. Preserve the original order of commands/outputs.

## DATA
(The DATA block contains failing commands/outputs followed by the fix commands/outputs.)
````md
    <issue_and_fix_data>
````

## TASK
Annotate the provided data by adding concise sentences for clear understanding. Identify and name the issue, then explain each fix step. Include the original commands and outputs unchanged under the appropriate sections. Follow the Example’s structure.

## RULES
- Give a proper name for the issue and place it as the H1 title at the top.
- The sentences describing the steps in the fix should be `Concise`, `Easily Understandable`, and `To the Point` (1-2 sentences per step).
- Follow the Example’s structure: H1 title, "Issue" section, "Fix" section, and numbered fix steps. Use fenced code blocks for commands/outputs.
- Return me with the whole response as a `Markdown` within **4 Backticks**(````<generated_content>````).
- Strictly keep the generated content within **4 Backticks**.

## EXAMPLE
Use the example below as a sample referenence to annotate the whole content.
````md
# PostgreSQL Service Startup Issue and Fix
## 🧾 Issue
**PostgreSQL service startup script not found**
When attempting to start PostgreSQL using a version‑specific init script, the system returns an error:
```bash
┌──(root㉿kali)-[~]
└─# /etc/init.d/postgresql-8.3 start
zsh: no such file or directory: /etc/init.d/postgresql-8.3
```
## 🛠️ Fix
### 1. Verify the installed PostgreSQL version
Check the currently installed PostgreSQL version to confirm the actual version in use:
```bash
┌──(root㉿kali)-[~]
└─# psql --version
psql (PostgreSQL) 17.5 (Debian 17.5-1)
```
The output shows that PostgreSQL 17.5 is installed, not 8.3.

### 2. Start the PostgreSQL service using the correct init/systemd command
Start the active PostgreSQL service directly, without specifying an outdated version number:
```bash
┌──(root㉿kali)-[~]
└─# /etc/init.d/postgresql start
Starting postgresql (via systemctl): postgresql.service
```
The message confirms that the service is managed by `systemctl` and has started successfully.
````

## RESPONSE RETURN FORMAT
````md
    <generated_markdown_content>
````
``````

# Example Prompt with Actual Data
``````md
## CONTEXT
I am reading a book named `Metasploit - The Penetration Tester's Guide`. While going through the chapters, I follow along with different commands to practice the implementation and analyze results. As this book is a little bit older, some commands mentioned there don't always work. So, whenever I fall into an issue, I fix that and proceed. I want to record the issue and the specific fix steps for future reference. I will provide only the raw commands and their outputs for one issue: failing commands/outputs first, then the fix commands/outputs. Do not add, remove, or modify any commands or outputs; annotate only. Preserve the original order of commands/outputs.

## DATA
(The DATA block contains failing commands/outputs followed by the fix commands/outputs.)
````md
## 🧾 Issue
```bash
msf6 > db_connect postgres:toor@127.0.0.1/msfbook
[-] Failed to connect to the Postgres data service: There is an issue connecting to your database with your username/password, username: postgres.

Please check your database configuration to ensure the username/password are valid.
```

## 🛠️ Fix
```bash
msf6 > sudo -u postgres psql
[*] exec: sudo -u postgres psql

psql (17.5 (Debian 17.5-1))
Type "help" for help.
```

```bash
postgres=# CREATE DATABASE msfbook OWNER postgres;
CREATE DATABASE
```

```bash
postgres=# \q
```

```bash
msf6 > db_connect postgres:toor@127.0.0.1/msfbook
[*] Connected to Postgres data service: 127.0.0.1/msfbook
```

```bash
msf6 > db_status
[*] Connected to msfbook. Connection type: postgresql. Connection name: local_db_service.
```
````

## TASK
Annotate the provided data by adding concise sentences for clear understanding. Identify and name the issue, then explain each fix step. Include the original commands and outputs unchanged under the appropriate sections. Follow the Example’s structure.

## RULES
- Give a proper name for the issue and place it as the H1 title at the top.
- The sentences describing the steps in the fix should be `Concise`, `Easily Understandable`, and `To the Point` (1-2 sentences per step).
- Follow the Example’s structure: H1 title, "Issue" section, "Fix" section, and numbered fix steps. Use fenced code blocks for commands/outputs.
- Return me with the whole response as a `Markdown` within **4 Backticks**(````<generated_content>````).
- Strictly keep the generated content within **4 Backticks**.

## EXAMPLE
Use the example below as a sample referenence to annotate the whole content.
````md
# PostgreSQL Service Startup Issue and Fix
## 🧾 Issue
**PostgreSQL service startup script not found**
When attempting to start PostgreSQL using a version‑specific init script, the system returns an error:
```bash
┌──(root㉿kali)-[~]
└─# /etc/init.d/postgresql-8.3 start
zsh: no such file or directory: /etc/init.d/postgresql-8.3
```
## 🛠️ Fix
### 1. Verify the installed PostgreSQL version
Check the currently installed PostgreSQL version to confirm the actual version in use:
```bash
┌──(root㉿kali)-[~]
└─# psql --version
psql (PostgreSQL) 17.5 (Debian 17.5-1)
```
The output shows that PostgreSQL 17.5 is installed, not 8.3.

### 2. Start the PostgreSQL service using the correct init/systemd command
Start the active PostgreSQL service directly, without specifying an outdated version number:
```bash
┌──(root㉿kali)-[~]
└─# /etc/init.d/postgresql start
Starting postgresql (via systemctl): postgresql.service
```
The message confirms that the service is managed by `systemctl` and has started successfully.
````

## RESPONSE RETURN FORMAT
````md
    <generated_markdown_content>
````
``````

# Expected Response from LLMs & Platforms
- **LLM**: `gpt-5-chat`<BR>**Platform**: `https://lmarena.ai/`