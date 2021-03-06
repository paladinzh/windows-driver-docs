---
title: KSPROPERTY\_DVDCOPY\_DEC\_KEY2
description: The KSPROPERTY\_DVDCOPY\_DEC\_KEY2 property retrieves the second bus key that is later provided to the decoder as part of the DVD copyright protection authentication process.
ms.assetid: 48e62fec-773d-46b6-838b-5e1e457cb6a3
keywords: ["KSPROPERTY_DVDCOPY_DEC_KEY2 Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_DVDCOPY_DEC_KEY2
api_location:
- ksmedia.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSPROPERTY\_DVDCOPY\_DEC\_KEY2


The KSPROPERTY\_DVDCOPY\_DEC\_KEY2 property retrieves the second bus key that is later provided to the decoder as part of the DVD copyright protection authentication process.

## <span id="ddk_ksproperty_dvdcopy_dec_key2_ks"></span><span id="DDK_KSPROPERTY_DVDCOPY_DEC_KEY2_KS"></span>


### <span id="Usage_Summary_Table"></span><span id="usage_summary_table"></span><span id="USAGE_SUMMARY_TABLE"></span>Usage Summary Table

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Get</th>
<th>Set</th>
<th>Target</th>
<th>Property descriptor type</th>
<th>Property value type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Yes</p></td>
<td><p>No</p></td>
<td><p>Pin</p></td>
<td><p>[<strong>KSPROPERTY</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564262)</p></td>
<td><p>[<strong>KS_DVDCOPY_BUSKEY</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567635)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a KS\_DVDCOPY\_BUSKEY structure that describes the DVD decoder's second bus key.

Remarks
-------

For more information about the second bus key, see [DVD Copyright Protection](https://msdn.microsoft.com/library/windows/hardware/ff558736).

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Header</p></td>
<td>Ksmedia.h (include Ksmedia.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**KS\_DVDCOPY\_BUSKEY**](https://msdn.microsoft.com/library/windows/hardware/ff567635)

 

 






