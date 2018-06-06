---
title: IOCTL\_CHANGER\_MOVE\_MEDIUM control code
description: Moves a piece of media from a source element to a destination.
ms.assetid: 4a410f56-cdc1-4cb0-801c-62402caec4ee
keywords:
- IOCTL_CHANGER_MOVE_MEDIUM control code Storage Devices
topic_type:
- apiref
api_name:
- IOCTL_CHANGER_MOVE_MEDIUM
api_location:
- Ntddchgr.h
api_type:
- HeaderDef
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# IOCTL\_CHANGER\_MOVE\_MEDIUM control code

Moves a piece of media from a source element to a destination.

## Input Buffer

The buffer at **Irp-&gt;AssociatedIrp.SystemBuffer** contains the [**CHANGER\_MOVE\_MEDIUM**](changer-move-medium.md) data, which indicates the transport to use for the operation, the source, the destination, and whether the medium should be flipped, assuming the device supports two-sided media.

## Input Buffer Length

**Parameters.DeviceIoControl.InputBufferLength** in the I/O stack location indicates the size, in bytes, of the parameter buffer, which must be &gt;= **sizeof**(CHANGER\_MOVE\_MEDIUM).

## Output Buffer

None.

## Output Buffer Length

None.

## Status block

The **Information** field is set to **sizeof**(CHANGER\_MOVE\_MEDIUM). The **Status** field is set to STATUS\_SUCCESS, or possibly to STATUS\_DESTINATION\_ELEMENT\_FULL, STATUS\_INFO\_LENGTH\_MISMATCH, STATUS\_INSUFFICIENT\_RESOURCES, STATUS\_INVALID\_DEVICE\_REQUEST, STATUS\_INVALID\_ELEMENT\_ADDRESS, STATUS\_INVALID\_PARAMETER, or STATUS\_SOURCE\_ELEMENT\_EMPTY.

## Requirements



|                   |                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ntddchgr.h (include Ntddchgr.h)</dt> </dl> |



## See also

<dl> <dt>

[**CHANGER\_MOVE\_MEDIUM**](changer-move-medium.md)
</dt> <dt>

[**ChangerMoveMedium**](changermovemedium.md)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstorage\storage%5D:%20IOCTL_CHANGER_MOVE_MEDIUM%20control%20code%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





