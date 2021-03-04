---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 99df3feae227aff03d49bfd029f34be4bc32d250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971117"
---
# <span data-ttu-id="3f786-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="3f786-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="3f786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f786-102">SYNOPSIS</span></span>
<span data-ttu-id="3f786-103">Eliminare un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="3f786-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3f786-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f786-104">SYNTAX</span></span>

### <span data-ttu-id="3f786-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3f786-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f786-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3f786-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f786-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3f786-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f786-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3f786-108">DESCRIPTION</span></span>
<span data-ttu-id="3f786-109">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="3f786-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3f786-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f786-110">EXAMPLES</span></span>

### <span data-ttu-id="3f786-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3f786-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="3f786-112">Eliminare un servizio di provisioning dei dispositivi Hub IoT di Azure 'myiotdps'.</span><span class="sxs-lookup"><span data-stu-id="3f786-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="3f786-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3f786-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="3f786-114">Eliminare un servizio di provisioning dei dispositivi Hub IoT di Azure 'myiotdps' usando una pipeline.</span><span class="sxs-lookup"><span data-stu-id="3f786-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="3f786-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f786-115">PARAMETERS</span></span>

### <span data-ttu-id="3f786-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f786-116">-DefaultProfile</span></span>
<span data-ttu-id="3f786-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f786-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f786-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f786-118">-InputObject</span></span>
<span data-ttu-id="3f786-119">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="3f786-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="3f786-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3f786-120">-Name</span></span>
<span data-ttu-id="3f786-121">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="3f786-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3f786-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f786-122">-PassThru</span></span>
<span data-ttu-id="3f786-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3f786-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3f786-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f786-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f786-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3f786-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3f786-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f786-126">-ResourceId</span></span>
<span data-ttu-id="3f786-127">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="3f786-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="3f786-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f786-128">-Confirm</span></span>
<span data-ttu-id="3f786-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f786-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f786-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f786-130">-WhatIf</span></span>
<span data-ttu-id="3f786-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f786-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f786-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f786-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f786-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f786-133">CommonParameters</span></span>
<span data-ttu-id="3f786-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f786-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f786-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f786-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f786-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="3f786-136">INPUTS</span></span>

### <span data-ttu-id="3f786-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3f786-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="3f786-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3f786-138">System.String</span></span>

## <span data-ttu-id="3f786-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f786-139">OUTPUTS</span></span>

### <span data-ttu-id="3f786-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f786-140">System.Boolean</span></span>

## <span data-ttu-id="3f786-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="3f786-141">NOTES</span></span>

## <span data-ttu-id="3f786-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f786-142">RELATED LINKS</span></span>
