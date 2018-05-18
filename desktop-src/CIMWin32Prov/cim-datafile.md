---
Description: 'The CIM\_DataFile class represents a named collection of data or executable code. Only instances of files on local fixed disks will be returned.'
audience: developer
author: 'REDMOND\\markl'
manager: 'REDMOND\\markl'
ms.assetid: 'e90e1216-e943-4f3a-9f6c-8a0b4568a11f'
ms.prod: 'windows-server-dev'
ms.technology:
- cimwin32
- 'windows-management-instrumentation'
ms.tgt_platform: multiple
title: 'CIM\_DataFile class'
---

# CIM\_DataFile class

The **CIM\_DataFile** class represents a named collection of data or executable code. Only instances of files on local fixed disks will be returned.

> \[!Important\]  
> The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built. WMI currently supports only the [CIM 2.x version schemas](Http://Go.Microsoft.Com/FWLink/p/?LinkID=309367).

�

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties. Properties are listed in alphabetic order, not MOF order.

## Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C55A-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("All Files (CIM)"), AMENDMENT]
class CIM_DataFile : CIM_LogicalFile
{
  string�� Caption;
  string�� Description;
  datetime InstallDate;
  string�� Status;
  uint32�� AccessMask;
  boolean� Archive;
  boolean� Compressed;
  string�� CompressionMethod;
  string�� CreationClassName;
  datetime CreationDate;
  string�� CSCreationClassName;
  string�� CSName;
  string�� Drive;
  string�� EightDotThreeFileName;
  boolean� Encrypted;
  string�� EncryptionMethod;
  string�� Name;
  string�� Extension;
  string�� FileName;
  uint64�� FileSize;
  string�� FileType;
  string�� FSCreationClassName;
  string�� FSName;
  boolean� Hidden;
  uint64�� InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string�� Path;
  boolean� Readable;
  boolean� System;
  boolean� Writeable;
  string�� Manufacturer;
  string�� Version;
};
```

## Members

The **CIM\_DataFile** class has these types of members:

-   [Methods](#methods)
-   [Properties](#properties)

### Methods

The **CIM\_DataFile** class has these methods.



| Method                                                                                          | Description                                                                                                                                          |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md)     | Changes the security permissions for the logical file specified in the object path. Implemented by WMI.<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-datafile.md) | Changes the security permissions for the logical file specified in the object path. Implemented by WMI.<br/>                                   |
| [**Compress**](compress-method-in-class-cim-datafile.md)                                       | Uses NTFS compression to compress the logical file (or directory) specified in the object path. Implemented by WMI.<br/>                       |
| [**CompressEx**](compressex-method-in-class-cim-datafile.md)                                   | Compresses the logical file (or directory) specified in the object path. Implemented by WMI.<br/>                                              |
| [**Copy**](copy-method-in-class-cim-datafile.md)                                               | Copies the logical file (or directory) specified in the object path to the location specified by the input parameter. Implemented by WMI.<br/> |
| [**CopyEx**](copyex-method-in-class-cim-datafile.md)                                           | Copies the logical file (or directory) specified in the object path to the location specified by the input parameter. Implemented by WMI.<br/> |
| [**Delete**](delete-method-in-class-cim-datafile.md)                                           | Deletes the logical file (or directory) specified in the object path. Implemented by WMI.<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-datafile.md)                                       | Deletes the logical file (or directory) specified in the object path. Implemented by WMI.<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-datafile.md)           | Determines whether the caller has the aggregated permissions specified by the **Permission** argument. Implemented by WMI.<br/>                |
| [**Rename**](rename-method-in-class-cim-datafile.md)                                           | Renames the logical file (or directory) specified in the object path. Implemented by WMI.<br/>                                                 |
| [**TakeOwnerShip**](takeownership-method-in-class-cim-datafile.md)                             | Obtains ownership of the logical file specified in the object path. Implemented by WMI.<br/>                                                   |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-datafile.md)                         | Obtains ownership of the logical file specified in the object path. Implemented by WMI.<br/>                                                   |
| [**Uncompress**](uncompress-method-in-class-cim-datafile.md)                                   | Uncompresses the logical file (or directory) specified in the object path. Implemented by WMI.<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-datafile.md)                               | Uncompresses the logical file (or directory) specified in the object path. Implemented by WMI.<br/>                                            |



�

### Properties

The **CIM\_DataFile** class has these properties.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Data type: **uint32**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Access Rights")
</dt> </dl>

Bitmask that represents the access rights required to access or perform specific operations on the file. For bit values, see [**File and Directory Access Rights Constants**](https://msdn.microsoft.com/library/aa822867).

> [!Note]  
> On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.

�

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**FILE\_READ\_EA** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**FILE\_WRITE\_EA** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**FILE\_DELETE\_CHILD (directory)** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**FILE\_READ\_ATTRIBUTES** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**FILE\_WRITE\_ATTRIBUTES** (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**DELETE** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**READ\_CONTROL** (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**WRITE\_DAC** (262144)


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**WRITE\_OWNER** (524288)


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**SYNCHRONIZE** (1048576)


</dt> <dd></dd> </dl>

</dd> <dt>

**Archive**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Should Be Archived")
</dt> </dl>

If **True**, the file should be archived.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MaxLen**](https://msdn.microsoft.com/library/aa393650) (64), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Caption")
</dt> </dl>

A short textual description of the object.

This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Compressed")
</dt> </dl>

If **True**, the file is compressed.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Compression Method")
</dt> </dl>

Free-form string that indicates the algorithm or tool used to compress the logical file. If the compression scheme is unknown or not described, use "Unknown". If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed". If the logical file is not compressed, use "Not Compressed".

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**CIM\_Key**](https://msdn.microsoft.com/library/aa393651), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Class Name")
</dt> </dl>

Name of the class.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Data type: **datetime**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Creation Date")
</dt> </dl>

Date and time of the file's creation.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Propagated**](https://msdn.microsoft.com/library/aa393650) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](https://msdn.microsoft.com/library/aa393651), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Computer System Class Name")
</dt> </dl>

Class of the computer system.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Propagated**](https://msdn.microsoft.com/library/aa393650) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](https://msdn.microsoft.com/library/aa393651), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Computer System Name")
</dt> </dl>

Name of the computer system.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Description")
</dt> </dl>

A textual description of the object.

This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Drive**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Fixed**](https://msdn.microsoft.com/library/aa393651), [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Drive")
</dt> </dl>

Drive letter (including the colon that follows the drive letter) of the file.

Example: "c:"

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Eight Dot Three File Name")
</dt> </dl>

DOS-compatible file name.

Example: "c:\\progra~1"

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Encrypted**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Encrypted")
</dt> </dl>

If **True**, the file is encrypted.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Encryption Method")
</dt> </dl>

Free-form string that identifies the algorithm or tool used to encrypt a logical file. If the encryption scheme is not indulged (for security reasons, for example), use "Unknown". If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted". If the logical file is not encrypted, use "Not Encrypted".

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Extension**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Fixed**](https://msdn.microsoft.com/library/aa393651), [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("File Extension")
</dt> </dl>

File name extension without the preceding period (dot).

Example: "txt", "mof", "mdb"

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Fixed**](https://msdn.microsoft.com/library/aa393651), [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("File Name")
</dt> </dl>

File name without the file name extension. Example: "MyDataFile"

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Data type: **uint64**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Size"), [**Units**](https://msdn.microsoft.com/library/aa393650) ("bytes")
</dt> </dl>

Size of the file, in bytes.

For more information about using **uint64** values in scripts, see [Scripting in WMI](https://msdn.microsoft.com/library/aa389763).

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("File Type")
</dt> </dl>

Descriptor that represents the file type indicated by the **Extension** property.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Propagated**](https://msdn.microsoft.com/library/aa393650) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](https://msdn.microsoft.com/library/aa393651), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("File System Class Name")
</dt> </dl>

Class of the file system.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Propagated**](https://msdn.microsoft.com/library/aa393650) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](https://msdn.microsoft.com/library/aa393651), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("File System Name")
</dt> </dl>

Name of the file system.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Hidden")
</dt> </dl>

If **True**, the file is hidden.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Data type: **datetime**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MappingStrings**](https://msdn.microsoft.com/library/aa393650) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Install Date")
</dt> </dl>

Indicates when the object was installed. Lack of a value does not indicate that the object is not installed.

This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Data type: **uint64**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Current File Open Count")
</dt> </dl>

Number of "file opens" that are currently active against the file.

For more information about using **uint64** values in scripts, see [Scripting in WMI](https://msdn.microsoft.com/library/aa389763).

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Data type: **datetime**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Last Accessed")
</dt> </dl>

Date and time the file was last accessed.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

Data type: **datetime**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Last Modified")
</dt> </dl>

Date and time the file was last modified.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Manufacturer")
</dt> </dl>

Manufacturer string from the version resource (if one is present).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Key**](https://msdn.microsoft.com/library/aa392157)
</dt> </dl>

The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system. Full path names should be provided.

Example: C:\\Windows\\system\\win.ini

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Fixed**](https://msdn.microsoft.com/library/aa393651), [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Path")
</dt> </dl>

Path of the file including the leading and trailing backslashes. Example: "\\windows\\system\\"

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Readable**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Readable")
</dt> </dl>

If **True**, the file can be read.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MaxLen**](https://msdn.microsoft.com/library/aa393650) (10), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Status")
</dt> </dl>

String that indicates the current status of the object. Operational and non-operational status can be defined. Operational status can include "OK", "Degraded", and "Pred Fail". "Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).

Non-operational status can include "Error", "Starting", "Stopping", and "Service". "Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work. Not all such work is online, but the managed element is neither "OK" nor in one of the other states.

This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).

Values include the following:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degraded** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unknown** ("Unknown")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Stopping** ("Stopping")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Service** ("Service")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**No Contact** ("No Contact")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> <dt>

**System**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("System File")
</dt> </dl>

If **True**, the file is a system file.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Schema**](https://msdn.microsoft.com/library/aa393650) ("Win32"), [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Version")
</dt> </dl>

Version string from the version resource (if one is present).

</dd> <dt>

**Writeable**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/library/aa393650) ("Writeable")
</dt> </dl>

If **True**, the file can be written.

This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).

</dd> </dl>

## Remarks

The **CIM\_DataFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).

WMI implements the **CIM\_DataFile** class and all of its methods. The **CIM\_DataFile** class is a dynamic class.

This documentation is derived from the CIM class descriptions published by the DMTF. Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.

Due to security purposes, WMI does not directly support calling a remote computer and instructing it to copy files to itself. However, you can use the relevant programming language to call FTP or RoboCopy, for example.

## Examples

The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) uses a **CIM\_DataFile** class as part of a larger application to Generate exchange environment reports using Powershell.

The [Find files with WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) code sample in TechNet Gallery uses a **CIM\_DataFile** to search for one or more files across multiple computers.

The following VBS code sample describes how to perform a standard wildcard search on a datafile. Note that the backslash delimiters must be escaped with another backslash (\\\\). Also, when using "**CIM\_DataFile**.**FileName**" in the WHERE clause, the WMIPRVSE process will scan all directories on any available storage device. This may take some time, especially if you have mapped remote shares, and can trigger antivirus warnings.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where FileName Like '%~%'")
For Each objFile in colFiles
   Wscript.Echo objFile.Name
Next
```



The following snippet limits the search range to a specific drive, path, and file extension.


```VB
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where Drive='"C:"' And Path='"\\"' and Name Like '%~%' and Extension='doc' ")
```



The following PowerShell code sample retrieves a single attribute value.


```PowerShell
 $computer = "."

  $path = "C:\\Program Files\\Microsoft SQL Server\\MSSQL.1\\MSSQL\\LOG\\"

  $filename = "ERRORLOG"

  $fullname = $path + $filename

  $wql = 'SELECT Archive FROM CIM_DataFile WHERE Name = "' + $fullname + '"'


  Get-WmiObject -ComputerName $computer -Query $wql | foreach { $_.Archive }
```



## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server�2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## See also

<dl> <dt>

[**CIM\_LogicalFile**](cim-logicalfile.md)
</dt> <dt>

[WMI Tasks: Files and Folders](https://msdn.microsoft.com/library/aa394594)
</dt> <dt>

[**File and Directory Access Rights Constants**](https://msdn.microsoft.com/library/aa822867)
</dt> </dl>

�

�



