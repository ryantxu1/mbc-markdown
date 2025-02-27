<table>
<tr>
<td><b>ID</b></td>
<td><b>F0009</b></td>
</tr>
<tr>
<td><b>Objective(s)</b></td>
<td><b><a href="../impact">Impact</a>, <a href="../persistence">Persistence</a>, <a href="../defense-evasion">Defense Evasion</a></b></td>
</tr>
<tr>
<td><b>Related ATT&CK Techniques</b></td>
<td><b>Pre-OS Boot: Component Firmware (<a href="https://attack.mitre.org/techniques/T1542/002/">1542.002</a>)</b></td>
</tr>
<tr>
<td><b>Impact Type</b></td>
<td><b>Breach</b></td>
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


# Component Firmware

Malware may overwrite the flash memory of firmware outside of the main system firmware or BIOS. [[1]](#1). Methods related to malware (extending ATT&CK's definitions) are below. 

See ATT&CK: **Pre-OS Boot: Component Firmware ([T1542.002](https://attack.mitre.org/techniques/T1542/002/))**.

## Methods

|Name|ID|Description|
|---|---|---|
|**Router Firmware**|F0009.001|Cisco routers can have their firmware images modified in order to maliciously infect and persist on end-user machines in a network. This is accomplished by using default or acquired credentials to gain access to a router and to install a backdoor. The implant resides within a modified Cisco IOS image and, when loaded, maintains its persistence in the environment, even after a system reboot. However, any further modules loaded by the attacker will only exist in the router's volatile memory and will not be available for use after reboot. Known affected hardware includes Cisco routers 1841, 2811, and 3825.|

## Use in Malware

|Name|Date|Method|Description|
|---|---|---|---|
|[**SYNful Knock**](../xample-malware/synful-knock.md)|2015|--|SYNful Knock is a stealthy modification of the router's firmware image that can be used to maintain persistence within a victim's network. [[2]](#2)|
|[**YiSpecter**](../xample-malware/yispecter.md)|2015|--|Displays brief advertisements whenever the user opens applications on their phone [[3]](#3)|
|[**SYNfulKnock**](../xample-malware/synful-knock.md)|2015|--|Modification of the router's firmware image that can be used to maintain persistence within a victim's network [[4]](#4)|

## References

<a name="1">[1]</a> https://www.scmagazine.com/home/opinions/are-synful-knock-style-router-attacks-set-to-become-the-new-normal/

<a name="2">[2]</a> https://www.fireeye.com/blog/threat-research/2015/09/synful_knock_-_acis.html

<a name="3">[3]</a> http://researchcenter.paloaltonetworks.com/2015/10/yispecter-first-ios-malware-attacks-non-jailbroken-ios-devices-by-abusing-private-apis/

<a name="4">[4]</a> https://www.mandiant.com/resources/synful-knock-acis
