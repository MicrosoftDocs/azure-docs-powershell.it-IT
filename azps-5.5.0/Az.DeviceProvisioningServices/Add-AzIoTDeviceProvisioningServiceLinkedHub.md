---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 30bcf61f309a400270e9cca378fce6d1149cf66a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200431"
---
# <span data-ttu-id="89a6c-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="89a6c-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="89a6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="89a6c-103">Hub IoT collegato a un servizio di provisioning di dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="89a6c-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="89a6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89a6c-104">SYNTAX</span></span>

### <span data-ttu-id="89a6c-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89a6c-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89a6c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="89a6c-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89a6c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="89a6c-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89a6c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="89a6c-108">DESCRIPTION</span></span>
<span data-ttu-id="89a6c-109">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="89a6c-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="89a6c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89a6c-110">EXAMPLES</span></span>

### <span data-ttu-id="89a6c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="89a6c-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="89a6c-112">Hub IoT collegato a un servizio di provisioning di dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="89a6c-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="89a6c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="89a6c-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="89a6c-114">Hub IoT collegato a un servizio di provisioning dei dispositivi Hub IoT di Azure con AllocationWeight e ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="89a6c-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="89a6c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89a6c-115">PARAMETERS</span></span>

### <span data-ttu-id="89a6c-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="89a6c-116">-AllocationWeight</span></span>
<span data-ttu-id="89a6c-117">Peso dell'allocazione dell'Hub IoT</span><span class="sxs-lookup"><span data-stu-id="89a6c-117">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a6c-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="89a6c-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="89a6c-119">Booleano che indica se applicare il criterio di assegnazione all'Hub IoT</span><span class="sxs-lookup"><span data-stu-id="89a6c-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a6c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a6c-120">-DefaultProfile</span></span>
<span data-ttu-id="89a6c-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89a6c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89a6c-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="89a6c-122">-DpsObject</span></span>
<span data-ttu-id="89a6c-123">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="89a6c-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="89a6c-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="89a6c-124">-IotHubConnectionString</span></span>
<span data-ttu-id="89a6c-125">Stringa di connessione della risorsa Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="89a6c-125">Connection String of the Iot Hub resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a6c-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="89a6c-126">-IotHubLocation</span></span>
<span data-ttu-id="89a6c-127">Posizione dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="89a6c-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a6c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="89a6c-128">-Name</span></span>
<span data-ttu-id="89a6c-129">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="89a6c-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="89a6c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89a6c-130">-ResourceGroupName</span></span>
<span data-ttu-id="89a6c-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="89a6c-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="89a6c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89a6c-132">-ResourceId</span></span>
<span data-ttu-id="89a6c-133">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="89a6c-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="89a6c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89a6c-134">-Confirm</span></span>
<span data-ttu-id="89a6c-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89a6c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a6c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89a6c-136">-WhatIf</span></span>
<span data-ttu-id="89a6c-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89a6c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89a6c-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89a6c-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a6c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a6c-139">CommonParameters</span></span>
<span data-ttu-id="89a6c-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89a6c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a6c-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89a6c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a6c-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="89a6c-142">INPUTS</span></span>

### <span data-ttu-id="89a6c-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="89a6c-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="89a6c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="89a6c-144">System.String</span></span>

## <span data-ttu-id="89a6c-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89a6c-145">OUTPUTS</span></span>

### <span data-ttu-id="89a6c-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="89a6c-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="89a6c-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="89a6c-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="89a6c-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="89a6c-148">NOTES</span></span>

## <span data-ttu-id="89a6c-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89a6c-149">RELATED LINKS</span></span>
