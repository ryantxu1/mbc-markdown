<table>
<tr>
<td><b>ID</b></td>
<td><b>E1059</b></td>
</tr>
<tr>
<td><b>Objective(s)</b></td>
<td><b><a href="../execution">Execution</a></b></td>
</tr>
<tr>
<td><b>Related ATT&CK Techniques</b></td>
<td><b>Command and Scripting Interpreter (<a href="https://attack.mitre.org/techniques/T1059">T1059</a>, <a href="https://attack.mitre.org/techniques/T1623">T1623</a>)</b></td>
</tr>
<tr>
<td><b>Version</b></td>
<td><b>2.0</b></td>
</tr>
<tr>
<td><b>Created</b></td>
<td><b>2 August 2022</b></td>
</tr>
<tr>
<td><b>Last Modified</b></td>
<td><b>21 November 2022</b></td>
</tr>
</table>


# Command and Scripting Interpreter

Malware may abuse command and script interpreters to execute commands, scripts, or binaries.

See ATT&CK: **Command and Scripting Interpreter ([T1059](https://attack.mitre.org/techniques/T1059), [T1623](https://attack.mitre.org/techniques/T1623))**.

## Use in Malware

|Name|Date|Method|Description|
|---|---|---|---|
|[**Poison-Ivy**](../xample-malware/poison-ivy.md)|2005|--|After the Poison-Ivy server is running on the target machine, the attacker can use a Windows GUI client to control the target computer. [[1]](#1)|
|[**WebCobra**](../xample-malware/webcobra.md)|2018|--|From the command line, drops and unzips a password-protected Cabinet archive file. [[1]](#1)|
|[**GotBotKR**](../xample-malware/gobotkr.md)|2019|--|GoBotKR uses cmd.exe to execute commands. [[2]](#2)|
|[**Kovter**](../xample-malware/kovter.md)|2016|--|The malware executes malicious javascript and powershell [[3]](#3)|
|[**SamSam**](../xample-malware/samsam.md)|2015|--|SamSam uses a batch file for executing the malware and deleting certain components   [[4]](#4)|
|[**Shamoon**](../xample-malware/shamoon.md)|2012|--|The wiper component of Shamoon creates a service to run the driver with the command: sc create hdv_725x type= kernel start= demand binpath= WINDOWS\hdv_725x.sys 2>&1 >nul and sends an additional reboot command after completion [[5]](#5)|
|[**Stuxnet**](../xample-malware/stuxnet.md)|2010|--|Stuxnet will store and execute SQL code that will extract and execute Stuxnet from the saved CAB file using xp_cmdshell  [[6]](#6)|
|[**EvilBunny**](../xample-malware/evilbunny.md)|2011|--|EvilBunny executes Lua scripts [[7]](#7)|
|[**Netwalker**](../xample-malware/netwalker.md)|2020|--|Netwalker is written and executed in Powershell [[8]](#8)|

## References

<a name="1">[1]</a> https://www.cyber.nj.gov/threat-profiles/trojan-variants/poison-ivy

<a name="2">[2]</a> https://www.welivesecurity.com/2019/07/08/south-korean-users-backdoor-torrents/

<a name="3">[3]</a> https://www.bleepingcomputer.com/virus-removal/remove-kovter-trojan

<a name="4">[4]</a> https://www.sophos.com/en-us/medialibrary/PDFs/technical-papers/SamSam-ransomware-chooses-Its-targets-carefully-wpna.pdf

<a name="5">[5]</a> https://www.mcafee.com/blogs/other-blogs/mcafee-labs/shamoon-returns-to-wipe-systems-in-middle-east-europe/

<a name="6">[6]</a> https://docs.broadcom.com/doc/security-response-w32-stuxnet-dossier-11-en

<a name="7">[7]</a> https://web.archive.org/web/20150311013500/http://www.cyphort.com/evilbunny-malware-instrumented-lua/

<a name="8">[8]</a> https://www.trendmicro.com/en_us/research/20/e/netwalker-fileless-ransomware-injected-via-reflective-loading.html