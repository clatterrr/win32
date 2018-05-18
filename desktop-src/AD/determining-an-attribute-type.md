---
title: Determining an Attribute Type
description: The systemFlags attribute of an attributeSchema object contains a set of flags that indicate various qualities of the attribute object, such as whether the attribute is constructed or non-replicated.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: '58f44ea4-ecbd-4650-b366-37b05a975c68'
ms.prod: 'windows-server-dev'
ms.technology: 'active-directory-domain-services'
ms.tgt_platform: multiple
keywords: ["Determining an Attribute Type AD"]
---

# Determining an Attribute Type

The [**systemFlags**](https://msdn.microsoft.com/library/ms680022) attribute of an [**attributeSchema**](https://msdn.microsoft.com/library/ms680969) object contains a set of flags that indicate various qualities of the attribute object, such as whether the attribute is constructed or non-replicated. The following table lists the flags of the **systemFlags** attribute that affect the storage type of the attribute. 

| Flag value | Description                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| 0x00000001 | If this flag is present in the [**systemFlags**](https://msdn.microsoft.com/library/ms680022) attribute, the attribute is not replicated. |
| 0x00000004 | If this flag is present in the [**systemFlags**](https://msdn.microsoft.com/library/ms680022) attribute, the attribute is constructed.    |



 

It is possible to construct a query string that can be used to query for constructed or non-replicated attributes. For example, the following query string finds all non-replicated [**attributeSchema**](https://msdn.microsoft.com/library/ms680969) objects. Be aware that the query string requires the decimal equivalent of the value, not the hexadecimal equivalent of the value. For more information about the matching rule OID used by this query string, see [How to Specify Comparison Values](how-to-specify-comparison-values.md).


```C++
(&amp;(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



The [**searchFlags**](https://msdn.microsoft.com/library/ms679765) attribute of each attribute's [**attributeSchema**](https://msdn.microsoft.com/library/ms680969) object defines whether an attribute is indexed; an indexed attribute has a value of 1, a non-indexed attribute has a value of 0. For example, the following query string finds the **attributeSchema** objects representing indexed attributes.


```C++
(&amp;(objectCategory=attributeSchema)(searchFlags=1))
```



The [**isMemberOfPartialAttributeSet**](https://msdn.microsoft.com/library/ms676807) attribute of each attribute's [**attributeSchema**](https://msdn.microsoft.com/library/ms680969) object defines whether an attribute is replicated to the global catalog. This attribute has a value of **TRUE** if the attribute is a member of the global catalog or **FALSE** if the attributes is not in the global catalog. For example, the following query string searches the **attributeSchema** objects that are replicated to the global catalog.


```C++
(&amp;(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 



