---
Description: 'Sent when current program chain (PGC) changes.'
ms.assetid: '80fcd059-6ab4-4116-ac3a-012c451237b3'
title: 'EC\_DVD\_PROGRAM\_CHAIN\_CHANGE'
---

# EC\_DVD\_PROGRAM\_CHAIN\_CHANGE

Sent when current program chain (PGC) changes.

## Parameters

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

The new program chain number (PGCN).

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

The locale identifier (LCID) of the audio language.

</dd> </dl>

## Remarks

This event is disabled by default. To enable this event, call [**IDvdControl2::SetOption**](idvdcontrol2-setoption.md) and set the **DVD\_NotifyPositionChange** option to **TRUE**.

## Requirements



|                   |                                                                                                          |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode.h (include Dshow.h)</dt> </dl> |



## See also

<dl> <dt>

[DVD Applications](dvd-applications.md)
</dt> <dt>

[DVD Event Notification Codes](dvd-notification-codes.md)
</dt> <dt>

[Event Notification in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

�

�



