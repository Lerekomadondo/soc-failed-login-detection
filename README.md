# SOC Lab: Failed Login Detection and Investigation

## Project Overview
This project demonstrates how to use Kusto Query Language (KQL) to detect and investigate repeated failed login attempts.

I used Azure Log Analytics and Microsoft Sentinel to practise security monitoring and investigation techniques with simulated authentication events.

## Tools Used
- Microsoft Azure
- Azure Log Analytics
- Microsoft Sentinel
- Kusto Query Language (KQL)
- GitHub

## Detection Scenario
The simulated dataset contains five failed login attempts for the user `john` from IP address `192.0.2.10`, followed by a successful login.

A KQL query identifies users and IP addresses with five or more failed login attempts.

## Investigation Findings
- **User:** john
- **Source IP:** 192.0.2.10
- **Failed attempts:** 5
- **First failed attempt:** 09:00
- **Last failed attempt:** 09:04
- **Subsequent successful login:** 09:05

This pattern may indicate repeated incorrect passwords or a possible brute-force attempt. It does not, by itself, confirm that the account was compromised.

## Repository Files
- `detection.kql` — identifies repeated failed login attempts.
- `investigation.kql` — reviews the authentication event timeline.
- `incident-report.md` — documents findings and recommended actions.

## Limitations
The authentication events are simulated. The queries demonstrate detection and investigation logic but are not connected to live logs and do not generate automated Sentinel alerts.

## Skills Demonstrated
- KQL query writing
- Authentication log analysis
- Failed-login detection
- Security investigation
- Incident reporting and documentation

## Future Improvements
- Connect a suitable live log source.
- Test the detection against real lab events.
- Configure and validate a Microsoft Sentinel analytics rule.


