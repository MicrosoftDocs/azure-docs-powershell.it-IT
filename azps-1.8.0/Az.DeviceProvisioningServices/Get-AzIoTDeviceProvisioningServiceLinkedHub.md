---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ec7f6e6bd402086084bee387be6a0563a6bf0c5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678882"
---
# <span data-ttu-id="4cf07-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="4cf07-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="4cf07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4cf07-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf07-103">Elenca tutti o Mostra i dettagli degli hub collegati in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="4cf07-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="4cf07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cf07-104">SYNTAX</span></span>

### <span data-ttu-id="4cf07-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4cf07-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf07-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4cf07-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf07-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4cf07-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cf07-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cf07-108">DESCRIPTION</span></span>
<span data-ttu-id="4cf07-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="4cf07-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="4cf07-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cf07-110">EXAMPLES</span></span>

### <span data-ttu-id="4cf07-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4cf07-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="4cf07-112">Elenca tutti gli hub degli elenchi collegati in "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="4cf07-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="4cf07-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4cf07-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="4cf07-114">Mostra i dettagli dell'hub collegato "myiothub1" in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="4cf07-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="4cf07-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4cf07-115">PARAMETERS</span></span>

### <span data-ttu-id="4cf07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf07-116">-DefaultProfile</span></span>
<span data-ttu-id="4cf07-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf07-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf07-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4cf07-118">-DpsObject</span></span>
<span data-ttu-id="4cf07-119">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="4cf07-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf07-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="4cf07-120">-LinkedHubName</span></span>
<span data-ttu-id="4cf07-121">Nome host dell'hub degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="4cf07-121">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf07-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cf07-122">-Name</span></span>
<span data-ttu-id="4cf07-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="4cf07-123">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf07-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf07-124">-ResourceGroupName</span></span>
<span data-ttu-id="4cf07-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4cf07-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf07-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cf07-126">-ResourceId</span></span>
<span data-ttu-id="4cf07-127">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="4cf07-127">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf07-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf07-128">CommonParameters</span></span>
<span data-ttu-id="4cf07-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf07-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf07-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cf07-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf07-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4cf07-131">INPUTS</span></span>

### <span data-ttu-id="4cf07-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4cf07-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4cf07-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4cf07-133">System.String</span></span>

## <span data-ttu-id="4cf07-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cf07-134">OUTPUTS</span></span>

### <span data-ttu-id="4cf07-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="4cf07-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="4cf07-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="4cf07-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="4cf07-137">Note</span><span class="sxs-lookup"><span data-stu-id="4cf07-137">NOTES</span></span>

## <span data-ttu-id="4cf07-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cf07-138">RELATED LINKS</span></span>