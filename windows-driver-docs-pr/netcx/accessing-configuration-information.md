---
title: Accessing configuration information
description: Accessing configuration information
ms.assetid: ABEC75AE-9CE3-4574-B388-BC48D2BC8154
keywords:
- NetAdapterCx accessing configuration information, NetCx accessing configuration information
ms.author: windowsdriverdev
ms.date: 06/05/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Accessing configuration information

[!include[NetAdapterCx Beta Prerelease](../netcx-beta-prerelease.md)]

The NetAdapterCx class extension supports a set of functions that provide access to client driver registry parameters.

Typically, the client driver reads configuration info from its [*EVT_WDF_DRIVER_DEVICE_ADD*](https://msdn.microsoft.com/library/windows/hardware/ff541693) callback function.

Start by calling [**NetAdapterOpenConfiguration**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netadapter/nf-netadapter-netadapteropenconfiguration) to get a handle to a configuration object.  You can then query it:

```C++
NETCONFIGURATION configuration;

status = NetAdapterOpenConfiguration(NetAdapter, WDF_NO_OBJECT_ATTRIBUTES, &configuration);
if (! NT_SUCCESS(status)) {
    return status;
}

status = NetConfigurationQueryUlong(configuration, NET_CONFIGURATION_QUERY_ULONG_NO_FLAGS, &SomeValue, &myvalue);

NetConfigurationClose(configuration);
```

There are `NetConfiguration*` functions for querying ULONG data, strings, multi-strings (similar to REG_MULTI_SZ), binary blobs, and software-configurable network addresses:

* [**NetConfigurationAssignBinary**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netconfiguration/nf-netconfiguration-netconfigurationassignbinary)
* [**NetConfigurationAssignMultiString**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netconfiguration/nf-netconfiguration-netconfigurationassignmultistring)
* [**NetConfigurationAssignUlong**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netconfiguration/nf-netconfiguration-netconfigurationassignulong)
* [**NetConfigurationAssignUnicodeString**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netconfiguration/nf-netconfiguration-netconfigurationassignunicodestring)
* [**NetConfigurationClose**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netconfiguration/nf-netconfiguration-netconfigurationclose)
* [**NetConfigurationOpenSubConfiguration**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netconfiguration/nf-netconfiguration-netconfigurationopensubconfiguration)
* [**NetConfigurationQueryBinary**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netconfiguration/nf-netconfiguration-netconfigurationquerybinary)
* [**NetConfigurationQueryMultiString**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netconfiguration/nf-netconfiguration-netconfigurationquerymultistring)
* [**NetConfigurationQueryLinkLayerAddress**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netconfiguration/nf-netconfiguration-netconfigurationquerylinklayeraddress)
* [**NetConfigurationQueryString**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netconfiguration/nf-netconfiguration-netconfigurationquerystring)
* [**NetConfigurationQueryUlong**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/netconfiguration/nf-netconfiguration-netconfigurationqueryulong)
