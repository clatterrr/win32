---
Description: 'Cancels the specified task.'
audience: developer
author: 'REDMOND\\danlep'
manager: 'REDMOND\\timlt'
ms.assetid: '4BF77D72-2A67-4343-845F-AB1F0F2F13C1'
ms.prod: 'windows-server-dev'
ms.technology: 'compute-cluster-pack'
ms.tgt_platform: multiple
title: Cancel Task
---

# Cancel Task

Cancels the specified task.

## Request

You can specify the Cancel Task request as follows.



| Method                      | Request URI                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------|
| POST (before HPC Pack 2016) | http://*head\_node\_name*:*port*/WindowsHPC/*HPC\_cluster\_name*/Job/*job\_identifier*/Task/*task\_identifier*/Cancel |
| POST (HPC Pack 2016)        | http://*head\_node\_name*:*port*/WindowsHPC/Job/*job\_identifier*/Task/*task\_identifier*/Cancel                      |



�

For instances of the REST web service that are hosted in Azure, the head node name should have a format of *Windows\_Azure\_service\_name*.cloudapp.net.

To get the name to use for an HPC cluster that runs at least Microsoft HPC Pack 2008 R2 with Service Pack 3 (SP3), use the [**Get Clusters**](get-clusters.md) operation.

### URI Parameters

You can specify the following additional parameters on the request URI.



| Parameter   | Description                                                                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Forced      | Optional. Specifies whether to stop the task immediately without using the grace period for canceling a task.<br/> True indicates that the task should stop immediately without using the grace period for canceling a task. False indicates that the task should use the grace period for canceling a task. The default value is False.<br/>                                |
| api-version | Optional. Specifies the version of the operation to use for this request. To specify Microsoft�HPC�Pack�2008�R2 with Service�Pack�3 (SP3), use a value of 2011-11-01. The minimum version that supports this URI parameter is Microsoft�HPC�Pack�2008�R2 with SP3.<br/> The value of this URI parameter is ignored if the request also contains the api-version header.<br/> |



�

### Request Headers

The following table describes required and optional request headers.



| Request Header | Description                                                                                                                                                                                                                                                                                                                                                                               |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| api-version    | Optional. Specifies the version of the operation to use for this request. To specify Microsoft�HPC�Pack�2008�R2 with SP3, use a value of 2011-11-01. The minimum version that supports this header is Microsoft�HPC�Pack�2008�R2 with SP3.<br/> The value specified in this header overrides the value specified in the api-version URI parameter if both are specified.<br/> |
| CCP\_Version   | Optional. Specifies the version of the operation to use for this request.<br/> Deprecated beginning with Microsoft HPC Pack 2008 R2 with Service Pack 3 (SP3).<br/>                                                                                                                                                                                                           |



�

### Request Body

The format of the request body is as follows.


```XML
<string xmlns="http://schemas.microsoft.com/2003/10/Serialization/">
Cancellation Message</string>
```



The request XML consists of a single string element that specifies a reason for the cancellation of the task. The maximum length of the string is 128 characters. If you do not want to specify a reason for the cancellation of the task, use an empty string element.

## Response

The response includes an HTTP status code and a set of response headers.

### Status Code

A successful operation returns status code 200 (OK). For more information about status codes, see [HttpStatusCode](https://msdn.microsoft.com/library/system.net.httpstatuscode.aspx).

The error response is dependent upon the api-version used in the request. If the api-version is not provided, or CCP\_Version is specified, then the error response will be an XML string (Note: The error message will vary based on the error):


```XML
<string xmlns="http://schemas.microsoft.com/2003/10/Serialization/">Error message text.</string>
```



If the api-version is 2011-11-01 or later, the error message will be a more descriptive XML response (Note: Values will vary based on the error):


```XML
<HpcWebServiceFault xmlns="http://schemas.microsoft.com/HPCS2008R2/common" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
  <Code>267386880</Code>
  <Message>Error message text.</Message>
  <Values i:nil="true" xmlns:a="http://schemas.datacontract.org/2004/07/System.Collections.Generic"/>
</HpcWebServiceFault>
```



### Response Headers

The response for this operation includes the following headers.



| Response Header         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| x-ms-hpc-authoritychain | A comma-separated list of RFC 1918 IP addresses that indicate the sequence of instances of the REST web service that the operation called in order from to right.<br/> Only responses from instances of the REST web service that are hosted on Azure contain this header. Responses from instances of the REST web service that are hosted on premise omit this header.<br/> This header is supported beginning with Microsoft HPC Pack 2008 R2 with SP3 and is not supported in previous versions.<br/> |



�

The response for this operation also includes standard HTTP headers. All standard headers conform to the [HTTP/1.1 protocol specification](http://www.w3.org/Protocols/rfc2616/rfc2616.mdl).

### Response Body

None.

## Requirements



|                    |                                                                                |
|--------------------|--------------------------------------------------------------------------------|
| Product<br/> | HPC Pack 2008 R2 with at least SP2, or a later version of HPC Pack.<br/> |



�

�



