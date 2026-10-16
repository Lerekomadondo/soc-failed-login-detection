# Incident Report: Repeated Failed Login Attempts

## 1. Overview
**Project:** SOC Failed Login Detection and Investigation  
**Tools:** Microsoft Sentinel, Azure Log Analytics and KQL  
**Data source:** Simulated authentication events

## 2. Alert Summary
A KQL detection query identified five failed login attempts for the user `john` from source IP address `192.0.2.10`.

The detection threshold was five or more failed attempts.

## 3. Investigation Timeline

| Time | User | Result |
|---|---|---|
| 09:00 | john | Failed |
| 09:01 | john | Failed |
| 09:02 | john | Failed |
| 09:03 | john | Failed |
| 09:04 | john | Failed |
| 09:05 | john | Successful |
| 09:06 | mary | Successful |

## 4. Findings
The simulated events show five consecutive failed login attempts followed by a successful login for `john`.

This pattern could be caused by repeated incorrect passwords or a brute-force attempt. The available data is not enough to confirm an account compromise.

## 5. Recommended Actions
1. Verify whether the successful login was legitimate.
2. Review available authentication records for unusual devices, locations or activity.
3. Investigate other events associated with the account and source IP.
4. Escalate suspected compromise according to the organisation's incident response procedures.

## 6. Limitations
The events in this project are simulated and do not represent a real security incident. The queries demonstrate detection and investigation logic; they are not connected to a live data source and do not generate automated Sentinel alerts.

## 7. Skills Demonstrated
- KQL query writing
- Authentication event analysis
- Failed-login detection
- Basic security investigation
- Incident reporting
