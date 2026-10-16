# SOC Lab: Failed Login Detection and Investigation

## Project Overview

This project demonstrates how to use Kusto Query Language (KQL) to identify and investigate repeated failed login attempts.

The lab was built using Microsoft Azure, Azure Log Analytics and Microsoft Sentinel. Simulated authentication events were used to practise detection and investigation techniques without connecting a live security data source.

## Objectives

- Write KQL queries to analyse authentication events.
- Detect repeated failed login attempts.
- Investigate login patterns and identify a subsequent successful login.
- Document findings and recommend appropriate security investigation steps.

## Tools Used

- Microsoft Sentinel
- Azure Log Analytics
- Kusto Query Language (KQL)
- GitHub

## Detection Scenario

The simulated dataset contains five failed login attempts for the user `john`, originating from `192.0.2.10`, followed by a successful login.

A KQL query identifies users and IP addresses associated with five or more failed attempts.

## Investigation Findings

- User: `john`
- Source IP: `192.0.2.10`
- Failed login attempts: 5
- First failed attempt: 09:00
- Last failed attempt: 09:04
- Subsequent successful login: 09:05

The pattern warrants further investigation but does not, by itself, prove that the account was compromised.

## Recommended Investigation Steps

1. Verify whether the successful login was legitimate.
2. Review authentication records and available device or location information.
3. Look for other suspicious activity associated with the account.
4. Escalate suspected compromise according to the organisation's incident response procedures.

## Limitations

All events in this project are simulated. The queries demonstrate detection logic but do not represent real attacks or real security incidents. No automated Microsoft Sentinel analytics rule or live alert was configured as part of this exercise.

## Skills Demonstrated

- KQL query development
- Authentication log analysis
- Detection logic
- Security incident investigation
- Technical documentation

## Future Improvements

- Connect a suitable live security log source.
- Test the detection against real lab events.
- Develop and validate a Microsoft Sentinel analytics rule.
- Explore alert investigation and incident response workflows.
