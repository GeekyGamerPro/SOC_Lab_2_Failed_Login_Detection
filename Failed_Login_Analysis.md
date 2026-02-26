# Failed Login Detection Lab – Day 2

## Objective
Simulate and detect failed login attempts on Ubuntu.

## Tools Used
- Ubuntu Linux VM
- Terminal
- sudo and auth.log
- grep command

## Evidence
1. `/var/log` directory view – Screenshot: `01_var_log_directory.png`
2. auth.log open in terminal – Screenshot: `02_auth_log_terminal_view.png`
3. Filtered failed password attempts – Screenshot: `04_authentication_failure_search.png`

## Findings
- No failed login attempts existed initially.
- Simulated 5 failed login attempts using `su vboxuser` with incorrect passwords.
- All attempts were captured in `/var/log/auth.log` using `grep -i "failure"`.

## Analysis
- The system correctly logs failed authentication attempts.
- Each log entry includes timestamp, user, TTY, and command attempted.
- Analysts can correlate timestamps and source users to detect potential brute-force attempts.

## Conclusion
- Failed login detection works as expected.
- Log filtering using `grep` is an effective method for small-scale log analysis.
- This lab demonstrates core SOC investigative skills: log inspection, filtering, and evidence documentation.
