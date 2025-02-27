<table>
<tr>
<td><b>ID</b></td>
<td><b>F0005</b></td>
</tr>
<tr>
<td><b>Objective(s)</b></td>
<td><b><a href="../defense-evasion">Defense Evasion</a>, <a href="../persistence">Persistence</a></b></td>
</tr>
<tr>
<td><b>Related ATT&CK Techniques</b></td>
<td><b>Hide Artifacts: Hidden Files and Directories (<a href="https://attack.mitre.org/techniques/T1564/001/">T1564.001</a>)</b></td>
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
<td><b>21 November 2022</b></td>
</tr>
</table>


# Hidden Files and Directories

Malware may hide files and folders to avoid detection and/or to persist on the system. See potential methods below. 

See ATT&CK: **Hide Artifacts: Hidden Files and Directories ([T1564.001](https://attack.mitre.org/techniques/T1564/001/))**.

## Methods

|Name|ID|Description|
|---|---|---|
|**Attribute**|F0005.003|Malware may change or choose an attribute to hide a file or directory.|
|**Extension**|F0005.001|Malware may change or use a particular file extension to hide a file.|
|**Location**|F0005.002|Malware may change or choose the location of itself, another file, or a directory to prevent detection.|
|**Timestamp**|F0005.004|Malware may change the timestamp on a file to prevent detection.|


## Use in Malware

|Name|Date|Method|Description|
|---|---|---|---|
|[**GotBotKR**](../xample-malware/gobotkr.md)|2019|--| GoBotKR stores itself in a file with Hidden and System attributes. [[1]](#1)|
|[**Shamoon**](../xample-malware/shamoon.md)|2012|--|Modifies target files' time to August 2012 as an antiforensic trick  [[2]](#2)|
|[**CHOPSTICK**](../xample-malware/chopstick.md)|2015|--|CHOPSTICK creates a hidden file for temporary storage [[3]](#3)|

## References

<a name="1">[1]</a> https://www.welivesecurity.com/2019/07/08/south-korean-users-backdoor-torrents/

<a name="2">[2]</a> https://www.mcafee.com/blogs/other-blogs/mcafee-labs/shamoon-returns-to-wipe-systems-in-middle-east-europe/

<a name="3">[]</a> https://www.fireeye.com/content/dam/fireeye-www/global/en/current-threats/pdfs/rpt-apt28.pdf