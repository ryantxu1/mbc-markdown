<table>
<tr>
<td><b>ID</b></td>
<td><b>F0010</b></td>
</tr>
<tr>
<td><b>Objective(s)</b></td>
<td><b><a href="../persistence">Persistence</a>, <a href="../privilege-escalation">Privilege Escalation</a></b></td>
</tr>
<tr>
<td><b>Related ATT&CK Techniques</b></td>
<td><b>Boot or Logon Autostart Execution: Kernel Modules and Extensions (<a href="https://attack.mitre.org/techniques/T1547/006/">T1547.006</a>)</b></td>
</tr>
<tr>
<td><b>Version</b></td>
<td><b>2.0</b></td>
</tr>
<tr>
<td><b>Created</b></td>
<td><b>1 August 2019</b></td>
</tr>
<tr>
<td><b>Last Modified</b></td>
<td><b>31 October 2022</b></td>
</tr>
</table>


# Kernel Modules and Extensions

Malware may use loadable kernel modules to persist on a system. For example, one type of module is the device driver, which allows the kernel to access hardware connected to the system. Malware may try to hide drivers or modules by creating them without a name.

See ATT&CK: **Boot or Logon Autostart Execution: Kernel Modules and Extensions ([T1547.006](https://attack.mitre.org/techniques/T1547/006/))**.

## Methods

|Name|ID|Description|
|---|---|---|
|**Device Driver**|F0010.001|Allows kernel to access hardware connected to the system.|
