---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: fc1b8bbe14fb35e7613ac1ed09ecf87624920081
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985136"
---
# <span data-ttu-id="d9f7a-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="d9f7a-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="d9f7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f7a-103">Eliminare un hub IoT collegato in un servizio di provisioning di dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d9f7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9f7a-104">SYNTAX</span></span>

### <span data-ttu-id="d9f7a-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9f7a-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9f7a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9f7a-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f7a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d9f7a-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9f7a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9f7a-108">DESCRIPTION</span></span>
<span data-ttu-id="d9f7a-109">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="d9f7a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d9f7a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9f7a-110">EXAMPLES</span></span>

### <span data-ttu-id="d9f7a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9f7a-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="d9f7a-112">Eliminare l'hub IoT collegato "myiothub" in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="d9f7a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d9f7a-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="d9f7a-114">Eliminare l'hub IoT collegato "myiothub" in un servizio di provisioning dei dispositivi Hub IoT di Azure tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="d9f7a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9f7a-115">PARAMETERS</span></span>

### <span data-ttu-id="d9f7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f7a-116">-DefaultProfile</span></span>
<span data-ttu-id="d9f7a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9f7a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9f7a-118">-InputObject</span></span>
<span data-ttu-id="d9f7a-119">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="d9f7a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d9f7a-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="d9f7a-120">-LinkedHubName</span></span>
<span data-ttu-id="d9f7a-121">Nome host dell'hub IoT collegato</span><span class="sxs-lookup"><span data-stu-id="d9f7a-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="d9f7a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d9f7a-122">-Name</span></span>
<span data-ttu-id="d9f7a-123">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="d9f7a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d9f7a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9f7a-124">-PassThru</span></span>
<span data-ttu-id="d9f7a-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d9f7a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d9f7a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f7a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d9f7a-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d9f7a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d9f7a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9f7a-128">-ResourceId</span></span>
<span data-ttu-id="d9f7a-129">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="d9f7a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d9f7a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9f7a-130">-Confirm</span></span>
<span data-ttu-id="d9f7a-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9f7a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9f7a-132">-WhatIf</span></span>
<span data-ttu-id="d9f7a-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9f7a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9f7a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f7a-135">CommonParameters</span></span>
<span data-ttu-id="d9f7a-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f7a-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9f7a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f7a-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9f7a-138">INPUTS</span></span>

### <span data-ttu-id="d9f7a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="d9f7a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="d9f7a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d9f7a-140">System.String</span></span>

## <span data-ttu-id="d9f7a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9f7a-141">OUTPUTS</span></span>

### <span data-ttu-id="d9f7a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d9f7a-142">System.Boolean</span></span>

## <span data-ttu-id="d9f7a-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9f7a-143">NOTES</span></span>

## <span data-ttu-id="d9f7a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9f7a-144">RELATED LINKS</span></span>
