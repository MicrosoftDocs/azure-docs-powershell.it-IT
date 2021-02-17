---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186014"
---
# <span data-ttu-id="c3cc1-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="c3cc1-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="c3cc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cc1-103">Elencare tutti gli hub IoT collegati o mostrarne i dettagli in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c3cc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3cc1-104">SYNTAX</span></span>

### <span data-ttu-id="c3cc1-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3cc1-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3cc1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3cc1-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3cc1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c3cc1-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3cc1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3cc1-108">DESCRIPTION</span></span>
<span data-ttu-id="c3cc1-109">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="c3cc1-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c3cc1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3cc1-110">EXAMPLES</span></span>

### <span data-ttu-id="c3cc1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c3cc1-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="c3cc1-112">Elencare tutti gli hub IoT collegati in "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="c3cc1-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="c3cc1-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c3cc1-113">Example 2</span></span>
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

<span data-ttu-id="c3cc1-114">Visualizzare i dettagli dell'hub IoT collegato "myiothub1" in un servizio di provisioning di dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c3cc1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3cc1-115">PARAMETERS</span></span>

### <span data-ttu-id="c3cc1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3cc1-116">-DefaultProfile</span></span>
<span data-ttu-id="c3cc1-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3cc1-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c3cc1-118">-DpsObject</span></span>
<span data-ttu-id="c3cc1-119">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="c3cc1-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c3cc1-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="c3cc1-120">-LinkedHubName</span></span>
<span data-ttu-id="c3cc1-121">Nome host dell'hub IoT collegato</span><span class="sxs-lookup"><span data-stu-id="c3cc1-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="c3cc1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c3cc1-122">-Name</span></span>
<span data-ttu-id="c3cc1-123">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="c3cc1-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c3cc1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3cc1-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3cc1-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c3cc1-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c3cc1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3cc1-126">-ResourceId</span></span>
<span data-ttu-id="c3cc1-127">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="c3cc1-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c3cc1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cc1-128">CommonParameters</span></span>
<span data-ttu-id="c3cc1-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cc1-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3cc1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cc1-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3cc1-131">INPUTS</span></span>

### <span data-ttu-id="c3cc1-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c3cc1-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c3cc1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c3cc1-133">System.String</span></span>

## <span data-ttu-id="c3cc1-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3cc1-134">OUTPUTS</span></span>

### <span data-ttu-id="c3cc1-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="c3cc1-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="c3cc1-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="c3cc1-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="c3cc1-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3cc1-137">NOTES</span></span>

## <span data-ttu-id="c3cc1-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3cc1-138">RELATED LINKS</span></span>
