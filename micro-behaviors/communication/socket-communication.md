<table>
<tr>
<td><b>ID</b></td>
<td><b>C0001</b></td>
</tr>
<tr>
<td><b>Objective(s)</b></td>
<td><b><a href="../communication">Communication</a></b></td>
</tr>
<tr>
<td><b>Related ATT&CK Techniques</b></td>
<td><b>None</b></td>
</tr>
<tr>
<td><b>Version</b></td>
<td><b>3.0</b></td>
</tr>
<tr>
<td><b>Created</b></td>
<td><b>25 September 2020</b></td>
</tr>
<tr>
<td><b>Last Modified</b></td>
<td><b>21 November 2022</b></td>
</tr>
</table>


# Socket Communication

This micro-behavior focuses on socket (TCP, UDP) communication. 

Instead of being listed alphabetically, methods have been grouped to better faciliate labeling and mapping.

## Methods

|Name|ID|Description|
|---|---|---|
|**Set Socket Config**|C0001.001|Configure socket.|
|**Initialize Winsock Library**|C0001.009|Winsock is initialized for TCP communication.|
|**Start TCP Server**|C0001.005|A TCP server listens for client requests.|
|**Create Socket**|C0001.003|A server or client creates a UDP or TCP socket.|
|**Create UDP Socket**|C0001.010|A UDP socket is created.|
|**Create TCP Socket**|C0001.011|A TCP socket is created.|
|**Connect Socket**|C0001.004|A server or client connects via a TCP socket.|
|**Get Socket Status**|C0001.012|Get socket status.|
|**Send Data**|C0001.007|Send data on socket.|
|**Send TCP Data**|C0001.014|Send TCP data.|
|**Send UDP Data**|C0001.015|Send UDP data.|
|**Receive Data**|C0001.006|Receive data on socket.|
|**Receive TCP Data**|C0001.016|Receive TCP data.|
|**Receive UDP Data**|C0001.017|Receive UDP data.|
|**TCP Server**|C0001.002|TCP server behavior.|
|**TCP Client**|C0001.008|TCP client behavior.|
|**UDP Client**|C0001.013|UDP client behavior.|


## Use in Malware

|Name|Date|Method|Description|
|---|---|---|---|
|[**SYNfulKnock**](../../xample-malware/synful-knock.md)|2015|--|To initiate communication with the C2 server, a uniquely crafted TCP SYN packet is sent to port 80 of the "implanted" router  [[1]](#1)|


## References

<a name="1">[1]</a> https://www.mandiant.com/resources/synful-knock-acis
