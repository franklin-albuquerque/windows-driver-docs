---
title: KSPROPERTY\_VIDEOPROCAMP\_HUE
description: The KSPROPERTY\_VIDEOPROCAMP\_HUE property controls the hue setting of the camera. This property is optional.
keywords: ["KSPROPERTY_VIDEOPROCAMP_HUE Streaming Media Devices"]
topic_type:
- apiref
ms.topic: reference
api_name:
- KSPROPERTY_VIDEOPROCAMP_HUE
api_location:
- Ksmedia.h
api_type:
- HeaderDef
ms.date: 11/28/2017
---

# KSPROPERTY\_VIDEOPROCAMP\_HUE


The KSPROPERTY\_VIDEOPROCAMP\_HUE property controls the hue setting of the camera. This property is optional.

## <span id="ddk_ksproperty_videoprocamp_hue_ks"></span><span id="DDK_KSPROPERTY_VIDEOPROCAMP_HUE_KS"></span>


### Usage Summary Table

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
<td><p>Yes</p></td>
<td><p>Filter or node</p></td>
<td><p><a href="/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksproperty_videoprocamp_s" data-raw-source="[&lt;strong&gt;KSPROPERTY_VIDEOPROCAMP_S&lt;/strong&gt;](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksproperty_videoprocamp_s)"><strong>KSPROPERTY_VIDEOPROCAMP_S</strong></a> or <a href="/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksproperty_videoprocamp_node_s" data-raw-source="[&lt;strong&gt;KSPROPERTY_VIDEOPROCAMP_NODE_S&lt;/strong&gt;](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksproperty_videoprocamp_node_s)"><strong>KSPROPERTY_VIDEOPROCAMP_NODE_S</strong></a></p></td>
<td><p>LONG</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a LONG that specifies a camera's hue setting. The value of the hue setting is expressed in degrees multiplied by 100.

## Remarks

The **Value** member of the KSPROPERTY\_VIDEOPROCAMP\_S structure specifies the hue setting.

Every video capture minidriver must define a range and default value for the **Value** member of this property. The required range must be -18000 to 18000 (-180 to +180 degrees). The default value must be 0.

## Requirements

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

## See also


[**KSPROPERTY**](ksproperty-structure.md)

[**KSPROPERTY\_VIDEOPROCAMP\_S**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksproperty_videoprocamp_s)

