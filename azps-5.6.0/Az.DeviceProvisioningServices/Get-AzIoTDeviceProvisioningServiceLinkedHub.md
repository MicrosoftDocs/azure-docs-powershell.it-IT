---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 5aff957c16fa6fefb52706f70016092a37cdcb3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980445"
---
# <span data-ttu-id="434fb-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="434fb-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="434fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="434fb-102">SYNOPSIS</span></span>
<span data-ttu-id="434fb-103">Elencare tutti gli hub IoT collegati o mostrarne i dettagli in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="434fb-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="434fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="434fb-104">SYNTAX</span></span>

### <span data-ttu-id="434fb-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="434fb-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="434fb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="434fb-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="434fb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="434fb-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="434fb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="434fb-108">DESCRIPTION</span></span>
<span data-ttu-id="434fb-109">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="434fb-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="434fb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="434fb-110">EXAMPLES</span></span>

### <span data-ttu-id="434fb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="434fb-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="434fb-112">Elencare tutti gli hub IoT collegati in "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="434fb-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="434fb-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="434fb-113">Example 2</span></span>
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

<span data-ttu-id="434fb-114">Visualizzare i dettagli dell'hub IoT collegato "myiothub1" in un servizio di provisioning di dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="434fb-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="434fb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="434fb-115">PARAMETERS</span></span>

### <span data-ttu-id="434fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434fb-116">-DefaultProfile</span></span>
<span data-ttu-id="434fb-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="434fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="434fb-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="434fb-118">-DpsObject</span></span>
<span data-ttu-id="434fb-119">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="434fb-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="434fb-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="434fb-120">-LinkedHubName</span></span>
<span data-ttu-id="434fb-121">Nome host dell'hub IoT collegato</span><span class="sxs-lookup"><span data-stu-id="434fb-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="434fb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="434fb-122">-Name</span></span>
<span data-ttu-id="434fb-123">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="434fb-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="434fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="434fb-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="434fb-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="434fb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="434fb-126">-ResourceId</span></span>
<span data-ttu-id="434fb-127">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="434fb-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="434fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434fb-128">CommonParameters</span></span>
<span data-ttu-id="434fb-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="434fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434fb-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="434fb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434fb-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="434fb-131">INPUTS</span></span>

### <span data-ttu-id="434fb-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="434fb-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="434fb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="434fb-133">System.String</span></span>

## <span data-ttu-id="434fb-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="434fb-134">OUTPUTS</span></span>

### <span data-ttu-id="434fb-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="434fb-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="434fb-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="434fb-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="434fb-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="434fb-137">NOTES</span></span>

## <span data-ttu-id="434fb-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="434fb-138">RELATED LINKS</span></span>
