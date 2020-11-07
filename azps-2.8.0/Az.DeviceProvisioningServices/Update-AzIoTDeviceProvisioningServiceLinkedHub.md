---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: d941e59c3d0681b91cdef9d05617c665dcc83177
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674524"
---
# <span data-ttu-id="3cc5a-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="3cc5a-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="3cc5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3cc5a-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc5a-103">Aggiorna un hub collegato agli aggiornamenti in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="3cc5a-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3cc5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cc5a-104">SYNTAX</span></span>

### <span data-ttu-id="3cc5a-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3cc5a-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc5a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3cc5a-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc5a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3cc5a-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc5a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cc5a-108">DESCRIPTION</span></span>
<span data-ttu-id="3cc5a-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="3cc5a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3cc5a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cc5a-110">EXAMPLES</span></span>

### <span data-ttu-id="3cc5a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3cc5a-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="3cc5a-112">Aggiornare l'hub degli aggiornamenti collegati "myiothub.azure-devices.net" in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="3cc5a-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3cc5a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3cc5a-113">PARAMETERS</span></span>

### <span data-ttu-id="3cc5a-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="3cc5a-114">-AllocationWeight</span></span>
<span data-ttu-id="3cc5a-115">Peso dell'allocazione dell'hub</span><span class="sxs-lookup"><span data-stu-id="3cc5a-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="3cc5a-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3cc5a-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="3cc5a-117">Applicare criteri di allocazione all'hub molto</span><span class="sxs-lookup"><span data-stu-id="3cc5a-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="3cc5a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc5a-118">-DefaultProfile</span></span>
<span data-ttu-id="3cc5a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3cc5a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cc5a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cc5a-120">-InputObject</span></span>
<span data-ttu-id="3cc5a-121">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="3cc5a-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cc5a-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="3cc5a-122">-LinkedHubName</span></span>
<span data-ttu-id="3cc5a-123">Nome host dell'hub degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="3cc5a-123">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cc5a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3cc5a-124">-Name</span></span>
<span data-ttu-id="3cc5a-125">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="3cc5a-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3cc5a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc5a-126">-ResourceGroupName</span></span>
<span data-ttu-id="3cc5a-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3cc5a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3cc5a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cc5a-128">-ResourceId</span></span>
<span data-ttu-id="3cc5a-129">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3cc5a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="3cc5a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3cc5a-130">-Confirm</span></span>
<span data-ttu-id="3cc5a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cc5a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc5a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc5a-132">-WhatIf</span></span>
<span data-ttu-id="3cc5a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cc5a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cc5a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cc5a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc5a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc5a-135">CommonParameters</span></span>
<span data-ttu-id="3cc5a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc5a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc5a-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc5a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc5a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3cc5a-138">INPUTS</span></span>

### <span data-ttu-id="3cc5a-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="3cc5a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="3cc5a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3cc5a-140">System.String</span></span>

## <span data-ttu-id="3cc5a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cc5a-141">OUTPUTS</span></span>

### <span data-ttu-id="3cc5a-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="3cc5a-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="3cc5a-143">Note</span><span class="sxs-lookup"><span data-stu-id="3cc5a-143">NOTES</span></span>

## <span data-ttu-id="3cc5a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cc5a-144">RELATED LINKS</span></span>