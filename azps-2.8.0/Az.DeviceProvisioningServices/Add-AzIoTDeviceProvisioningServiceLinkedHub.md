---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 346a09a635b72612c270889afd904a1535994624
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674555"
---
# <span data-ttu-id="fa78d-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="fa78d-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="fa78d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa78d-102">SYNOPSIS</span></span>
<span data-ttu-id="fa78d-103">Hub molto collegato a un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="fa78d-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="fa78d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa78d-104">SYNTAX</span></span>

### <span data-ttu-id="fa78d-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa78d-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa78d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa78d-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa78d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fa78d-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa78d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa78d-108">DESCRIPTION</span></span>
<span data-ttu-id="fa78d-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="fa78d-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="fa78d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa78d-110">EXAMPLES</span></span>

### <span data-ttu-id="fa78d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fa78d-111">Example 1</span></span>
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

<span data-ttu-id="fa78d-112">Hub molto collegato a un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="fa78d-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="fa78d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fa78d-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="fa78d-114">Hub molto collegato a un servizio di provisioning del dispositivo hub di Azure molto con AllocationWeight e ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="fa78d-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="fa78d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa78d-115">PARAMETERS</span></span>

### <span data-ttu-id="fa78d-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="fa78d-116">-AllocationWeight</span></span>
<span data-ttu-id="fa78d-117">Peso dell'allocazione dell'hub</span><span class="sxs-lookup"><span data-stu-id="fa78d-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="fa78d-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="fa78d-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="fa78d-119">Valore booleano che indica se applicare i criteri di allocazione all'hub molto</span><span class="sxs-lookup"><span data-stu-id="fa78d-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="fa78d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa78d-120">-DefaultProfile</span></span>
<span data-ttu-id="fa78d-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa78d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa78d-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="fa78d-122">-DpsObject</span></span>
<span data-ttu-id="fa78d-123">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="fa78d-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="fa78d-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="fa78d-124">-IotHubConnectionString</span></span>
<span data-ttu-id="fa78d-125">Stringa di connessione della risorsa Hub molto.</span><span class="sxs-lookup"><span data-stu-id="fa78d-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="fa78d-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="fa78d-126">-IotHubLocation</span></span>
<span data-ttu-id="fa78d-127">Posizione dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="fa78d-127">Location of the Iot Hub</span></span>

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

### <span data-ttu-id="fa78d-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa78d-128">-Name</span></span>
<span data-ttu-id="fa78d-129">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="fa78d-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fa78d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa78d-130">-ResourceGroupName</span></span>
<span data-ttu-id="fa78d-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fa78d-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fa78d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa78d-132">-ResourceId</span></span>
<span data-ttu-id="fa78d-133">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="fa78d-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="fa78d-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fa78d-134">-Confirm</span></span>
<span data-ttu-id="fa78d-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa78d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa78d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa78d-136">-WhatIf</span></span>
<span data-ttu-id="fa78d-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa78d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa78d-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa78d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa78d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa78d-139">CommonParameters</span></span>
<span data-ttu-id="fa78d-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa78d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa78d-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa78d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa78d-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa78d-142">INPUTS</span></span>

### <span data-ttu-id="fa78d-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="fa78d-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="fa78d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fa78d-144">System.String</span></span>

## <span data-ttu-id="fa78d-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa78d-145">OUTPUTS</span></span>

### <span data-ttu-id="fa78d-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="fa78d-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="fa78d-147">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="fa78d-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="fa78d-148">Note</span><span class="sxs-lookup"><span data-stu-id="fa78d-148">NOTES</span></span>

## <span data-ttu-id="fa78d-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa78d-149">RELATED LINKS</span></span>
