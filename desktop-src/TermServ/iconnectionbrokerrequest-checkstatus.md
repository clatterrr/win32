---
title: IConnectionBrokerRequest CheckStatus method
description: Called to determine the status of an asynchronous request.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: '6B0DDDB2-9905-4B48-8CCB-D6A6591B7723'
ms.prod: 'windows-server-dev'
ms.technology: 'remote-desktop-services'
ms.tgt_platform: multiple
keywords: ["CheckStatus method Remote Desktop Services", "CheckStatus method Remote Desktop Services , IConnectionBrokerRequest interface", "IConnectionBrokerRequest interface Remote Desktop Services , CheckStatus method"]
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
---

# IConnectionBrokerRequest::CheckStatus method

Called to determine the status of an asynchronous request.

## Syntax


```C++
HRESULT CheckStatus(
  [out]�CB_REQUEST_STATUS *pReqStatus
);
```



## Parameters

<dl> <dt>

*pReqStatus* \[out\]
</dt> <dd>

The address of a variable that receives a value of the [**CB\_REQUEST\_STATUS**](cb-request-status.md) enumeration that indicates the status of the request.

</dd> </dl>

## Return value

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�8<br/>                                                                    |
| Minimum supported server<br/> | Windows Server�2012<br/>                                                          |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl>   |
| Library<br/>                  | <dl> <dt>Cbclient.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## See also

<dl> <dt>

[**IConnectionBrokerRequest**](iconnectionbrokerrequest.md)
</dt> </dl>

�

�




