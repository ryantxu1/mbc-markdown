<table>
<tr>
<td><b>ID</b></td>
<td><b>B0025</b></td>
</tr>
<tr>
<td><b>Objective(s)</b></td>
<td><b><a href="../execution">Execution</a>, <a href="../anti-behavioral-analysis">Anti-Behavioral Analysis</a>, <a href="../defense-evasion">Defense Evasion</a></b></td>
</tr>
<tr>
<td><b>Related ATT&CK Techniques</b></td>
<td><b>Execution Guardrails  (<a href="https://attack.mitre.org/techniques/T1480">T1480</a>)</b></td>
</tr>
<tr>
<td><b>Anti-Analysis Type</b></td>
<td><b>Evasion</b></td>
</tr>
<tr>
<td><b>Version</b></td>
<td><b>3.0</b></td>
</tr>
<tr>
<td><b>Created</b></td>
<td><b>1 August 2019</b></td>
</tr>
<tr>
<td><b>Last Modified</b></td>
<td><b>21 November 2022</b></td>
</tr>
</table>


# Conditional Execution

Malware checks system environment conditions or characteristics to determine execution path. For example, malware may not run or be dormant unless system conditions are right, or file that is dropped may vary according to execution environment. Conditional execution in malware happens autonomously, not because of an attacker's command.

This behavior is related to the **Dynamic Analysis Evasion ([B0003](../anti-behavioral-analysis/dynamic-analysis-evasion.md))** behavior that obstructs dynamic analysis in a sandbox, emulator, or virtual machine.

Some aspects of this Conditional Execution behavior are related to the [Execution Guardrails (T1480)](https://attack.mitre.org/techniques/T1480) ATT&CK technique; however the ATT&CK technique is not focused on anti-behavioral analysis behaviors.

## Methods

|Name|ID|Description|
|---|---|---|
|**Deposited Keys**|B0025.008|Parts of the code and/or data is encrypted or otherwise relies on data external to the file itself. For example, malware that contains code that is encrypted with a key that is downloaded from a server; malware that only runs if certain other software is installed on the system. Also see Environmental Keys Method.|
|**Environmental Keys**|B0025.002|Malware reads certain attributes of the system (BIOS version string, hostname, MAC address, etc.) and encrypts/decrypts portions of its code or data using those attributes as input, thus preventing itself from being run on an unintended system (e.g., sandbox, emulator, etc.). Also see Deposited Keys Method. The subsequently defined ATT&CK sub-technique [Execution Guardrails: Environmental Keying (T1480.001)](https://attack.mitre.org/techniques/T1480/001/) is related to this MBC method. |
|**GetVolumeInformation**|B0025.003|This Windows API call is used to get the GUID on a system drive. Malware compares it to a previous (targeted) GUID value and only executes maliciously if they match. This behavior can be mitigated in non-automated analysis environments.|
|**Host Fingerprint Check**|B0025.004|Compare a previously computed host fingerprint(e.g., based on installed applications) to the current system's to determine if the malware instance is still executing on the same system. If not, execution stops, making debugging or sandbox analysis more difficult.|
|**Runs as Service**|B0025.007|The malware must be run as a service, which can make behavioral analysis and debugging more difficult. The service may be set up by the malware. Alternatively, the malware may not contain any code to create a new service or modify an existing service, in which case, the service may be set up by another program or manually. [[2]](#2)|
|**Secure Triggers**|B0025.005|Code and/or data is encrypted until the underlying system satisfies a preselected condition unknown to the analyst (this is a form of Deposited Keys).|
|**Suicide Exit**|B0025.001|Malware terminates its execution based on a trigger condition or value (or because it has completed).|
|**Token Check**|B0025.006|Presence check to allow the program to run (ex: dongle, CD/DVD, key, file, network, etc.). If the token is specific to a hardware element (ex: disk, OS, CPU, NIC MAC, etc.), it is considered fingerprinting.|

## Use in Malware

|Name|Date|Method|Description|
|---|---|---|---|
|[**WebCobra**](../xample-malware/webcobra.md)|2018|--|Drops either Cryptonight or Claymore's Zcash miner, depending on system architecture. [[1]](#1)|
|[**Conficker**](../xample-malware/conficker.md)|2008|--|A routine causes the process to suicide exit if the keyboard language is set to Ukranian.|
|[**Ursnif**](../xample-malware/ursnif.md)|2016|--|Macros check if there are at least 50 running processes with a graphical interface, check if a list of blacklisted processes are running, and checks if the application is running in Australia and is NOT affiliated with a select group of networks (Security Research, Hospitals, Universities, Veterans, etc.) [1] [[3]](#3)|
|[**Mebromi**](../xample-malware/mebromi.md)|2011|--|Malware only proceeds if it detects the BIOS ROM is Award BIOS [[4]](#4)|

## References

<a name="1">[1]</a> https://securingtomorrow.mcafee.com/other-blogs/mcafee-labs/webcobra-malware-uses-victims-computers-to-mine-cryptocurrency/

<a name="2">[2]</a> 
https://reverseengineering.stackexchange.com/questions/2019/debugging-malware-that-will-only-run-as-a-service

<a name="3">[3]</a> https://www.proofpoint.com/us/threat-insight/post/ursnif-banking-trojan-campaign-sandbox-evasion-techniques

<a name="4">[4]</a> https://www.webroot.com/blog/2011/09/13/mebromi-the-first-bios-rootkit-in-the-wild/
